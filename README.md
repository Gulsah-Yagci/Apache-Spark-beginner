# Apache-Spark-beginner

# İçerik

1. [Apache Spark](#1)


<a id=1></a><br>
# Apache Spark
Apache Spark açık kaynaklı dağıtılmış genel amaçlı bir küme bilgi işlem çerçevesi. Spark, örtülü veri paralelliği ve hata toleransı ile tüm kümeleri programlamak için bir arayüz sağlar.

* Bütünleşik bir hesaplama motoru

* Bilgisayar kümelerinde(cluster) paralel veri işleme için bir dizi kütüphane

***Bütünleşik bir hesaplama motoru nedir?***

Büyük veri uygulamaları için her türlü ihtiyacı karşılayacak şekilde tasarlanmış ve geliştirilmiş olmasıdır.

Veri okuma/yazma, programlama,SQL, makine öğrenmesi, streaming, graf analizi,python,scala, java ,R ... hepsi aynı motor ve birbiriyle uyumlu API setleri içindedir.

Spark bir hesaplama motorudur. Bütünleşiktir, birçok aracı barındırır ama sınırlarını da iyi çizer. Veri depolamaz. Veriyi olduğu yerde analiz eder. Gerektiği kadarını Spark Cluster belleğine çeker.

Bilgisayarların belleklerini kullanabildiği gibi, RAM'leri ve İşlemcilerini de dağıtık bir şekilde kullanır.

Spark, Hadoop Map Reduce'un varisidir. Bazı problemlerini özellikle hız konusundakileri çözüm getirmiştir. Hadoop ile uyumlu ancak çalışması için şart değildir.

## Spark vs MapReduce

* İkisi de Hadoop YARN üzerinde çalışabilir.

* Spark 100 kata kadar daha hızlı çalışabilir.

* Spark Hadoop'a bağımlı değildir.

* Spark belleği iyi kullanır, MapReduce diske bağımlıdır.

* Spark Scala,Java,Python ve R dillerini destekler.

* Spark'la geliştiriciler daha verimli çalışabilir.

* İnteraktif olarak kullanılabilir.

* Spark'ın daha az I/O organizasyonu ihtiyacı var.

* Spark'ta shuffle daha uygun maliyetli

## Çalışma Modları

Cluster Mode: Spark Standalone Cluster

Apache Mesos

Hadoop YARN

Kuberbetes

Local Mode: Basit geliştirmeler

## Spark Uygulaması Bileşenler

Çalışacak kod

Cluster Manager (YARN,Mesos,Kubernetes)

Worker sunucularda çalışan worker process'ler

Worker sunucularda çalışan executor'lar

Worker sunucularda çalışan task'lar

Mevcut bir veriyi parçalayıp cluster üzerine dağıtarak

numbers = sc.parallelize((1,2,3,4,5,6,7,8))

## RDD Operasyonları

Transformation - RDD transformation yapan ve sonuç olarak Başka bir RDD verir.

map()

filter()

flatMap()

sample()

repartition()

join()

Action - RDD'lerden bir sonuç üretir.

reduce()

collect()

count()

take()

saveAsTextFile()

takeSample()

## SparkConf
Uygulamanın çalışacağı ortam ile ilgili konfigürasyon bilgilerini tutan nesne.

## SparkContext - Kullanıcı ile etkileşim kapısı
Oluşturulan kon nesnesi SparkContext içinde kullanırız.

Cluster'a ne şekilde erişileceğiyle ilgili nesne.

RDD, Accumulator ve broadcast variables yaratmak için kullanılır.

Spark 2.0'dan önce Spark'a tek giriş noktasıydı.

Spark 2.0'dan sonra SparkContext ve SqlContext, SparkSession da birleşti.

## Low Level API (RDD Based)
Spark-1'de kullanılan en eski ve en düşük seviyeli API.

Spark-2 ile birlikte Structured API geldi ve kullanımı azaldı. Ancak hala Spark- 2'de kullanılabilir.

Structured API da kolaylıkla yapılan işler RDD'de daha zor ve uzun.

Python kullanıcı tanımlı fonksiyonları Scala'ya göre yavaş.
