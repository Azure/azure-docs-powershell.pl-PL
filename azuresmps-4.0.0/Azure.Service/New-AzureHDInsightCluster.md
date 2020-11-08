---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3EDD612F-AC5D-4D4D-BB14-2FB8DE5EDCCE
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4652cb1b30717b5ea11d596646dc43e2a5ec4a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054889"
---
# <span data-ttu-id="f625d-101">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f625d-101">New-AzureHDInsightCluster</span></span>

## <span data-ttu-id="f625d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f625d-102">SYNOPSIS</span></span>
<span data-ttu-id="f625d-103">Tworzy klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f625d-103">Creates an HDInsight cluster.</span></span>

## <span data-ttu-id="f625d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f625d-104">SYNTAX</span></span>

### <span data-ttu-id="f625d-105">Klaster według konfiguracji (z określonymi poświadczeniami abonamentu) (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f625d-105">Cluster By Config (with Specific Subscription Credential) (Default)</span></span>
```
New-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>]
 -Config <AzureHDInsightConfig> -Credential <PSCredential> [-EndPoint <Uri>] [-IgnoreSslErrors <Boolean>]
 -Location <String> -Name <String> [-Subscription <String>] [-Version <String>] [-OSType <OSType>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f625d-106">Klaster według nazwy (z określonymi poświadczeniami subskrypcji)</span><span class="sxs-lookup"><span data-stu-id="f625d-106">Cluster By Name (with Specific Subscription Credential)</span></span>
```
New-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>]
 -ClusterSizeInNodes <Int32> -Credential <PSCredential> -DefaultStorageAccountKey <String>
 -DefaultStorageAccountName <String> -DefaultStorageContainerName <String> [-EndPoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String> [-Subscription <String>] [-Version <String>]
 [-HeadNodeVMSize <String>] [-ClusterType <ClusterType>] [-VirtualNetworkId <String>] [-SubnetName <String>]
 [-DataNodeVMSize <String>] [-ZookeeperNodeVMSize <String>] [-OSType <OSType>] [-SshCredential <PSCredential>]
 [-SshPublicKey <String>] [-RdpCredential <PSCredential>] [-RdpAccessExpiry <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f625d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f625d-107">DESCRIPTION</span></span>
<span data-ttu-id="f625d-108">Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="f625d-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="f625d-109">Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.</span><span class="sxs-lookup"><span data-stu-id="f625d-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="f625d-110">Użyj nowszej wersji usługi HDInsight Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f625d-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="f625d-111">Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="f625d-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="f625d-112">Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="f625d-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="f625d-113">Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f625d-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="f625d-114">Polecenie cmdlet **New-AzureHDInsightCluster** tworzy klaster usługi Azure HDInsight przy użyciu określonych parametrów lub obiektu konfiguracji utworzonego za pomocą polecenia cmdlet **New-AzureHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="f625d-114">The **New-AzureHDInsightCluster** cmdlet creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>

## <span data-ttu-id="f625d-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f625d-115">EXAMPLES</span></span>

### <span data-ttu-id="f625d-116">Przykład 1. Tworzenie klastra usługi HDInsight</span><span class="sxs-lookup"><span data-stu-id="f625d-116">Example 1: Create an HDInsight cluster</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential 
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
    | Set-AzureHDInsightDefaultStorage -StorageAccountName "MyBlobStorage.blob.core.windows.net" -StorageAccountKey $Key1 -StorageContainerName "MyContainer" 
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds
```

<span data-ttu-id="f625d-117">W tym przykładzie jest tworzony klaster usługi HDInsight dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f625d-117">This example creates an HDInsight cluster for the current subscription.</span></span>

<span data-ttu-id="f625d-118">W pierwszym poleceniu jest używany polecenie cmdlet **Get-AzureSubscription** w celu uzyskania bieżącego identyfikatora subskrypcji, a następnie zapisanie go w zmiennej $SubId.</span><span class="sxs-lookup"><span data-stu-id="f625d-118">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="f625d-119">Drugie i trzecie polecenia cmdlet **Get-AzureStorageKey** umożliwiają uzyskiwanie podstawowych kluczy magazynu dla MyBlobStorage i MySecondBlobStorage, a następnie przechowywanie kluczy odpowiednio w zmiennych $Key 1 i $Key 2.</span><span class="sxs-lookup"><span data-stu-id="f625d-119">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="f625d-120">W przypadku czterech, piątych i szóstych poleceń Użyj polecenia cmdlet **Get-Credential** , aby uzyskać poświadczenia dla bieżącego abonamentu oraz dla Oozie i gałąź, a następnie zapisać poświadczenia w zmiennych.</span><span class="sxs-lookup"><span data-stu-id="f625d-120">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="f625d-121">Polecenie ostatnie wykonuje sekwencję operacji, korzystając z następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f625d-121">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="f625d-122">**New-AzureHDInsightClusterConfig** , aby utworzyć konfigurację klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f625d-122">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="f625d-123">**Set-AzureHDInsightDefaultStorage** , aby ustawić domyślne konto magazynu dla konfiguracji na MyBlobStorage.blob.Core.Windows.NET.</span><span class="sxs-lookup"><span data-stu-id="f625d-123">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="f625d-124">**Add-AzureHDInsightStorage** , aby dodać do konfiguracji drugie konto magazynu o nazwie MySecondBlobStorage.blob.Core.Windows.NET.</span><span class="sxs-lookup"><span data-stu-id="f625d-124">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="f625d-125">**Add-AzureHDInsightMetastore** , aby dodać do konfiguracji element magazynu dla Oozie i magazynu.</span><span class="sxs-lookup"><span data-stu-id="f625d-125">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="f625d-126">**New-AzureHDInsightCluster** , aby utworzyć klaster usługi HDInsight z nową konfiguracją.</span><span class="sxs-lookup"><span data-stu-id="f625d-126">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="f625d-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f625d-127">PARAMETERS</span></span>

### <span data-ttu-id="f625d-128">-Certificate</span><span class="sxs-lookup"><span data-stu-id="f625d-128">-Certificate</span></span>
<span data-ttu-id="f625d-129">Określa certyfikat zarządzania dla subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f625d-129">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625d-130">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="f625d-130">-ClusterSizeInNodes</span></span>
<span data-ttu-id="f625d-131">Określa liczbę węzłów danych do utworzenia dla klastra.</span><span class="sxs-lookup"><span data-stu-id="f625d-131">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Nodes, Size

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625d-132">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="f625d-132">-ClusterType</span></span>
<span data-ttu-id="f625d-133">Określa typ klastra do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="f625d-133">Specifies the type of cluster to create.</span></span>

```yaml
Type: ClusterType
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625d-134">-Config</span><span class="sxs-lookup"><span data-stu-id="f625d-134">-Config</span></span>
<span data-ttu-id="f625d-135">Określa obiekt konfiguracji utworzony za pomocą polecenia cmdlet **New-AzureHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="f625d-135">Specifies a configuration object that is created by using the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: Cluster By Config (with Specific Subscription Credential)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f625d-136">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="f625d-136">-Credential</span></span>
<span data-ttu-id="f625d-137">Określa poświadczenia użytkownika dla usługi HDInsight do użycia dla konta domyślnego, które jest używane do zdalnego uzyskiwania dostępu do klastra usługi Hadoop.</span><span class="sxs-lookup"><span data-stu-id="f625d-137">Specifies the user credentials for HDInsight to use for the default account that is used to remotely access a Hadoop cluster.</span></span>
<span data-ttu-id="f625d-138">Te poświadczenia różnią się od poświadczeń abonamentu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f625d-138">These credentials are distinct from the subscription credentials of the user.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: Cred

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625d-139">-DataNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="f625d-139">-DataNodeVMSize</span></span>
<span data-ttu-id="f625d-140">Określa rozmiar maszyny wirtualnej dla węzła danych.</span><span class="sxs-lookup"><span data-stu-id="f625d-140">Specifies the size of the virtual machine for the data node.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625d-141">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f625d-141">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="f625d-142">Określa klucz konta dla domyślnego konta magazynu używanego przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f625d-142">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625d-143">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f625d-143">-DefaultStorageAccountName</span></span>
<span data-ttu-id="f625d-144">Określa nazwę domyślnego konta magazynu używanego przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f625d-144">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625d-145">-DefaultStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="f625d-145">-DefaultStorageContainerName</span></span>
<span data-ttu-id="f625d-146">Określa nazwę kontenera domyślnego w domyślnym koncie magazynu platformy Azure używanym przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f625d-146">Specifies the name of the default container in the default Azure storage account that an HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625d-147">-EndPoint</span><span class="sxs-lookup"><span data-stu-id="f625d-147">-EndPoint</span></span>
<span data-ttu-id="f625d-148">Określa punkt końcowy, którego należy użyć w celu nawiązania połączenia z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f625d-148">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="f625d-149">Jeśli nie podano tego parametru, to polecenie cmdlet używa domyślnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="f625d-149">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625d-150">-HeadNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="f625d-150">-HeadNodeVMSize</span></span>
<span data-ttu-id="f625d-151">Określa rozmiar maszyny wirtualnej dla węzła głównego.</span><span class="sxs-lookup"><span data-stu-id="f625d-151">Specifies the size of the virtual machine for the head node.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625d-152">-HostedService</span><span class="sxs-lookup"><span data-stu-id="f625d-152">-HostedService</span></span>
<span data-ttu-id="f625d-153">Określa obszar nazw usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f625d-153">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="f625d-154">Jeśli nie podano tego parametru, to polecenie cmdlet użyje domyślnego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="f625d-154">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625d-155">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="f625d-155">-IgnoreSslErrors</span></span>
<span data-ttu-id="f625d-156">Wskazuje, czy są ignorowane błędy protokołu SSL (Secure Sockets Layer).</span><span class="sxs-lookup"><span data-stu-id="f625d-156">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625d-157">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f625d-157">-Location</span></span>
<span data-ttu-id="f625d-158">Określa region, w którym ma zostać utworzony klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f625d-158">Specifies the region in which to create an HDInsight cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Loc

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625d-159">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f625d-159">-Name</span></span>
<span data-ttu-id="f625d-160">Określa nazwę klastra usługi Azure HDInsight do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="f625d-160">Specifies the name of the Azure HDInsight cluster to create.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Config (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625d-161">-OSType</span><span class="sxs-lookup"><span data-stu-id="f625d-161">-OSType</span></span>
<span data-ttu-id="f625d-162">Określa system operacyjny dla klastra.</span><span class="sxs-lookup"><span data-stu-id="f625d-162">Specifies the operating system for a cluster.</span></span>

```yaml
Type: OSType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625d-163">-Profile</span><span class="sxs-lookup"><span data-stu-id="f625d-163">-Profile</span></span>
<span data-ttu-id="f625d-164">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f625d-164">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f625d-165">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="f625d-165">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625d-166">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="f625d-166">-RdpAccessExpiry</span></span>
<span data-ttu-id="f625d-167">Określa wygaśnięcie jako obiekt **DateTime** , aby uzyskać dostęp do klastra za pomocą protokołu RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="f625d-167">Specifies the expiration, as a **DateTime** object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625d-168">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="f625d-168">-RdpCredential</span></span>
<span data-ttu-id="f625d-169">Określa poświadczenia dostępu RDP do klastra.</span><span class="sxs-lookup"><span data-stu-id="f625d-169">Specifies the credentials for RDP access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625d-170">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="f625d-170">-SshCredential</span></span>
<span data-ttu-id="f625d-171">Określa nazwę użytkownika i hasło dla klastra usługi HDInsight (Secure Shell).</span><span class="sxs-lookup"><span data-stu-id="f625d-171">Specifies the Secure Shell (SSH) user name and password for the HDInsight cluster.</span></span>
<span data-ttu-id="f625d-172">Ten parametr jest prawidłowy tylko dla klastrów w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="f625d-172">This parameter is valid only for Linux clusters.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625d-173">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="f625d-173">-SshPublicKey</span></span>
<span data-ttu-id="f625d-174">Określa klucz publiczny SSH dla klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f625d-174">Specifies the SSH public key for an HDInsight cluster.</span></span>
<span data-ttu-id="f625d-175">Ten parametr jest prawidłowy tylko dla klastrów w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="f625d-175">This parameter is valid only for Linux clusters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625d-176">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="f625d-176">-SubnetName</span></span>
<span data-ttu-id="f625d-177">Określa nazwę podsieci.</span><span class="sxs-lookup"><span data-stu-id="f625d-177">Specifies the name of a subnet.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625d-178">-Subscription</span><span class="sxs-lookup"><span data-stu-id="f625d-178">-Subscription</span></span>
<span data-ttu-id="f625d-179">Określa subskrypcję platformy Azure, w której ma zostać utworzony klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f625d-179">Specifies the Azure subscription in which to create an HDInsight cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625d-180">-Version</span><span class="sxs-lookup"><span data-stu-id="f625d-180">-Version</span></span>
<span data-ttu-id="f625d-181">Określa wersję klastra usługi HDInsight do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="f625d-181">Specifies the HDInsight cluster version to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Ver

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625d-182">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="f625d-182">-VirtualNetworkId</span></span>
<span data-ttu-id="f625d-183">Określa identyfikator sieci wirtualnej, do której ma być zastrzec klaster.</span><span class="sxs-lookup"><span data-stu-id="f625d-183">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625d-184">-ZookeeperNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="f625d-184">-ZookeeperNodeVMSize</span></span>
<span data-ttu-id="f625d-185">Określa rozmiar maszyny wirtualnej dla węzła ZooKeeper.</span><span class="sxs-lookup"><span data-stu-id="f625d-185">Specifies the size of the virtual machine for the ZooKeeper node.</span></span>
<span data-ttu-id="f625d-186">Ten parametr jest prawidłowy tylko w przypadku klastrów HBase lub burzy.</span><span class="sxs-lookup"><span data-stu-id="f625d-186">This parameter is valid only for HBase or Storm clusters.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625d-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f625d-187">CommonParameters</span></span>
<span data-ttu-id="f625d-188">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f625d-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f625d-189">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f625d-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f625d-190">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f625d-190">INPUTS</span></span>

## <span data-ttu-id="f625d-191">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f625d-191">OUTPUTS</span></span>

## <span data-ttu-id="f625d-192">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f625d-192">NOTES</span></span>

## <span data-ttu-id="f625d-193">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f625d-193">RELATED LINKS</span></span>

[<span data-ttu-id="f625d-194">Dodaj-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="f625d-194">Add-AzureHDInsightMetastore</span></span>](./Add-AzureHDInsightMetastore.md)

[<span data-ttu-id="f625d-195">Dodaj-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="f625d-195">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="f625d-196">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f625d-196">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="f625d-197">Nowe — AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="f625d-197">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="f625d-198">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f625d-198">Remove-AzureHDInsightCluster</span></span>](./Remove-AzureHDInsightCluster.md)

[<span data-ttu-id="f625d-199">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="f625d-199">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)

[<span data-ttu-id="f625d-200">Użyj — AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f625d-200">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


