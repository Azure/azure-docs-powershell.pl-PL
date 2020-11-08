---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 600D35F8-1E3C-4724-9F5E-75CF754F424F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0809415ea5dfff687c69089e1aeda60c9f3b00ee
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054686"
---
# <span data-ttu-id="81b40-101">Add-AzureHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="81b40-101">Add-AzureHDInsightScriptAction</span></span>

## <span data-ttu-id="81b40-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="81b40-102">SYNOPSIS</span></span>
<span data-ttu-id="81b40-103">Dodaje akcję skryptu usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="81b40-103">Adds an HDInsight script action.</span></span>

## <span data-ttu-id="81b40-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="81b40-104">SYNTAX</span></span>

```
Add-AzureHDInsightScriptAction -Config <AzureHDInsightConfig> -Name <String>
 -ClusterRoleCollection <ClusterNodeType[]> -Uri <Uri> [-Parameters <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="81b40-105">Opis</span><span class="sxs-lookup"><span data-stu-id="81b40-105">DESCRIPTION</span></span>
<span data-ttu-id="81b40-106">Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="81b40-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="81b40-107">Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.</span><span class="sxs-lookup"><span data-stu-id="81b40-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="81b40-108">Użyj nowszej wersji usługi HDInsight Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="81b40-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="81b40-109">Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="81b40-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="81b40-110">Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="81b40-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="81b40-111">Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="81b40-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="81b40-112">Polecenie cmdlet **Add-AzureHDInsightScriptAction** oferuje funkcję HDInsight Azure, która służy do instalowania dodatkowego oprogramowania lub zmieniania konfiguracji aplikacji uruchomionych w klastrze usługi Hadoop za pomocą skryptów programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="81b40-112">The **Add-AzureHDInsightScriptAction** cmdlet provides Azure HDInsight functionality that is used to install additional software or to change the configuration of applications that run on a Hadoop cluster by using Windows PowerShell scripts.</span></span>

<span data-ttu-id="81b40-113">Akcja skryptu uruchamia się w węzłach klastra, gdy są wdrożone klastry usługi HDInsight i są uruchamiane po zakończeniu konfigurowania usługi HDInsight w klastrze.</span><span class="sxs-lookup"><span data-stu-id="81b40-113">A script action runs on the cluster nodes when HDInsight clusters are deployed, and they run after nodes in the cluster complete HDInsight configuration.</span></span>
<span data-ttu-id="81b40-114">Akcja skryptu jest uruchamiana w obszarze uprawnienia konta administratora systemu i zapewnia pełne prawa dostępu do węzłów klastra.</span><span class="sxs-lookup"><span data-stu-id="81b40-114">The script action runs under system administrator account privileges and provides full access rights to the cluster nodes.</span></span>
<span data-ttu-id="81b40-115">Możesz udostępnić każdemu klastrowi listę akcji skryptów do uruchomienia w określonej kolejności.</span><span class="sxs-lookup"><span data-stu-id="81b40-115">You can provide each cluster with a list of script actions to run in a specified sequence.</span></span>

## <span data-ttu-id="81b40-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="81b40-116">EXAMPLES</span></span>

### <span data-ttu-id="81b40-117">Przykład 1: Dodawanie akcji skryptu do klastra</span><span class="sxs-lookup"><span data-stu-id="81b40-117">Example 1: Add a script action to a cluster</span></span>
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction" -Uri http://test.com/test.ps1 -Parameters "test" -ClusterRoleCollection HeadNode,DataNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

<span data-ttu-id="81b40-118">W pierwszym poleceniu użyto polecenia cmdlet **New-AzureHDInsightClusterConfig** w celu utworzenia konfiguracji klastra usługi HDInsight, a następnie zapisu w zmiennej $config.</span><span class="sxs-lookup"><span data-stu-id="81b40-118">The first command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>

<span data-ttu-id="81b40-119">W drugim poleceniu użyto polecenia cmdlet **Add-AzureHDInsightScriptAction** w celu dodania akcji skryptu o nazwie TestScriptAction do $config.</span><span class="sxs-lookup"><span data-stu-id="81b40-119">The second command uses the **Add-AzureHDInsightScriptAction** cmdlet to add the script action named TestScriptAction to $Config.</span></span>

<span data-ttu-id="81b40-120">W poleceniu ostatnim użyto polecenia cmdlet **New-AzureHDInsightCluster** w celu utworzenia nowego klastra usługi HDInsight, który uruchamia akcję skryptu przechowywaną w $config.</span><span class="sxs-lookup"><span data-stu-id="81b40-120">The final command uses the **New-AzureHDInsightCluster** cmdlet to create a new HDInsight cluster that runs the script action stored in $Config.</span></span>

### <span data-ttu-id="81b40-121">Przykład 2: Dodawanie akcji wielu skryptów do klastra</span><span class="sxs-lookup"><span data-stu-id="81b40-121">Example 2: Add multiple script actions to a cluster</span></span>
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction1" -Uri http://test.com/test1.ps1 -Parameters "Test1" -ClusterRoleCollection HeadNode,DataNode | Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction2" -Uri http://test.com/test2.ps1 -ClusterRoleCollection HeadNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

<span data-ttu-id="81b40-122">W pierwszym poleceniu użyto polecenia cmdlet **New-AzureHDInsightClusterConfig** w celu utworzenia konfiguracji klastra usługi HDInsight, a następnie zapisu w zmiennej $config.</span><span class="sxs-lookup"><span data-stu-id="81b40-122">The first command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>

<span data-ttu-id="81b40-123">W drugim poleceniu użyto polecenia cmdlet **Add-AzureHDInsightScriptAction** , aby dodać określoną akcję skryptu do $config, a następnie użyć operatora potoku w celu przejścia $config do polecenia **Dodaj-AzureHDInsightScriptAction** po raz drugi w celu dodania drugiego skryptu do $config.</span><span class="sxs-lookup"><span data-stu-id="81b40-123">The second command uses the **Add-AzureHDInsightScriptAction** cmdlet to add the specified script action to $Config, and then uses the pipeline operator to pass $Config to **Add-AzureHDInsightScriptAction** a second time to add a second script action to $Config.</span></span>

<span data-ttu-id="81b40-124">W poleceniu ostatnim użyto polecenia cmdlet **New-AzureHDInsightCluster** w celu utworzenia klastra uruchamiającego akcje skryptu w $config.</span><span class="sxs-lookup"><span data-stu-id="81b40-124">The final command uses the **New-AzureHDInsightCluster** cmdlet to create a cluster that runs the script actions in $Config.</span></span>

## <span data-ttu-id="81b40-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="81b40-125">PARAMETERS</span></span>

### <span data-ttu-id="81b40-126">-ClusterRoleCollection</span><span class="sxs-lookup"><span data-stu-id="81b40-126">-ClusterRoleCollection</span></span>
<span data-ttu-id="81b40-127">Określa węzły, dla których ma zostać uruchomiony skrypt.</span><span class="sxs-lookup"><span data-stu-id="81b40-127">Specifies the nodes for which to run a script.</span></span>
<span data-ttu-id="81b40-128">Dopuszczalne wartości tego parametru to: HeadNode lub datanode.</span><span class="sxs-lookup"><span data-stu-id="81b40-128">The acceptable values for this parameter are: HeadNode or DataNode.</span></span>

<span data-ttu-id="81b40-129">Możesz określić pojedynczą wartość lub obie wartości.</span><span class="sxs-lookup"><span data-stu-id="81b40-129">You can specify one value or both values.</span></span>

```yaml
Type: ClusterNodeType[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b40-130">-Config</span><span class="sxs-lookup"><span data-stu-id="81b40-130">-Config</span></span>
<span data-ttu-id="81b40-131">Określa obiekt konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="81b40-131">Specifies a configuration object.</span></span>
<span data-ttu-id="81b40-132">To polecenie cmdlet umożliwia dodanie informacji o akcji skryptu do obiektu, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="81b40-132">This cmdlet adds script action information to the object that this parameter specifies.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81b40-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="81b40-133">-Name</span></span>
<span data-ttu-id="81b40-134">Określa nazwę akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="81b40-134">Specifies the name of a script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b40-135">— Parametry</span><span class="sxs-lookup"><span data-stu-id="81b40-135">-Parameters</span></span>
<span data-ttu-id="81b40-136">Określa parametry, które są wymagane przez akcję skryptu.</span><span class="sxs-lookup"><span data-stu-id="81b40-136">Specifies the parameters that are required by a script action.</span></span>

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

### <span data-ttu-id="81b40-137">-Profile</span><span class="sxs-lookup"><span data-stu-id="81b40-137">-Profile</span></span>
<span data-ttu-id="81b40-138">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81b40-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="81b40-139">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="81b40-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="81b40-140">-URI</span><span class="sxs-lookup"><span data-stu-id="81b40-140">-Uri</span></span>
<span data-ttu-id="81b40-141">Określa lokalizację URI skryptu, który ma być uruchomiony.</span><span class="sxs-lookup"><span data-stu-id="81b40-141">Specifies the URI location of a script to run.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b40-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81b40-142">CommonParameters</span></span>
<span data-ttu-id="81b40-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81b40-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81b40-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81b40-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81b40-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81b40-145">INPUTS</span></span>

## <span data-ttu-id="81b40-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="81b40-146">OUTPUTS</span></span>

## <span data-ttu-id="81b40-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="81b40-147">NOTES</span></span>

## <span data-ttu-id="81b40-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81b40-148">RELATED LINKS</span></span>

[<span data-ttu-id="81b40-149">Nowe — AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="81b40-149">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="81b40-150">Nowe — AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="81b40-150">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)


