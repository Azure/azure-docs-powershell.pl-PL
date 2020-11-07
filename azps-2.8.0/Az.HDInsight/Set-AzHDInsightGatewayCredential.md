---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightgatewaycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
ms.openlocfilehash: 045b0db296a9c3bde4332ce755c055d1e8616738
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705297"
---
# <span data-ttu-id="4a9c3-101">Set-AzHDInsightGatewayCredential</span><span class="sxs-lookup"><span data-stu-id="4a9c3-101">Set-AzHDInsightGatewayCredential</span></span>

## <span data-ttu-id="4a9c3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4a9c3-102">SYNOPSIS</span></span>
<span data-ttu-id="4a9c3-103">Ustawia poświadczenia HTTP bramy klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4a9c3-103">Sets the gateway HTTP credentials of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="4a9c3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4a9c3-104">SYNTAX</span></span>

### <span data-ttu-id="4a9c3-105">SetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4a9c3-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightGatewayCredential -Name <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a9c3-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a9c3-106">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -InputObject <AzureHDInsightCluster> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4a9c3-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a9c3-107">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a9c3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4a9c3-108">DESCRIPTION</span></span>
<span data-ttu-id="4a9c3-109">Polecenie cmdlet **Set-AzHDInsightGatewayCredential** ustawia poświadczenie bramy klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4a9c3-109">The **Set-AzHDInsightGatewayCredential** cmdlet sets gateway credential of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="4a9c3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4a9c3-110">EXAMPLES</span></span>

### <span data-ttu-id="4a9c3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4a9c3-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Set-AzHDInsightGatewayCredential `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="4a9c3-112">To polecenie ustawia poświadczenia bramy dla klastra o nazwie Your-Hadoop-001-Name Set.</span><span class="sxs-lookup"><span data-stu-id="4a9c3-112">This command sets gateway credential of the cluster named your-hadoop-001 by name parameter set.</span></span>

### <span data-ttu-id="4a9c3-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4a9c3-113">Example 2</span></span>
```powershell
PS C:\> Set-AzHDInsightGatewayCredential `
            -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.HDInsight/clusters/your-hadoop-001" `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="4a9c3-114">To polecenie ustawia poświadczenie bramy dla klastra o nazwie z ustawionym parametrem ResourceId.</span><span class="sxs-lookup"><span data-stu-id="4a9c3-114">This command sets gateway credential of the cluster named your-hadoop-001 by ResourceId parameter set.</span></span>

### <span data-ttu-id="4a9c3-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="4a9c3-115">Example 3</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Get-AzHDInsightCluster -ClusterName $clusterName | Set-AzHDInsightGatewayCredential `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="4a9c3-116">To polecenie ustawia poświadczenia bramy dla klastra o nazwie Your-Hadoop-001 według zestawu parametrów Inputobject.</span><span class="sxs-lookup"><span data-stu-id="4a9c3-116">This command sets gateway credential of the cluster named your-hadoop-001 by InputObject parameter set.</span></span>

## <span data-ttu-id="4a9c3-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4a9c3-117">PARAMETERS</span></span>

### <span data-ttu-id="4a9c3-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a9c3-118">-AsJob</span></span>
<span data-ttu-id="4a9c3-119">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="4a9c3-119">Run cmdlet in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a9c3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a9c3-120">-DefaultProfile</span></span>
<span data-ttu-id="4a9c3-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4a9c3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a9c3-122">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="4a9c3-122">-HttpCredential</span></span>
<span data-ttu-id="4a9c3-123">Pobiera lub ustawia identyfikator logowania dla użytkownika klastra.</span><span class="sxs-lookup"><span data-stu-id="4a9c3-123">Gets or sets the login for the cluster's user.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a9c3-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4a9c3-124">-InputObject</span></span>
<span data-ttu-id="4a9c3-125">Pobiera lub ustawia obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="4a9c3-125">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a9c3-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4a9c3-126">-Name</span></span>
<span data-ttu-id="4a9c3-127">Pobiera lub ustawia nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="4a9c3-127">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a9c3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a9c3-128">-ResourceGroupName</span></span>
<span data-ttu-id="4a9c3-129">Pobiera lub ustawia nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4a9c3-129">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a9c3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a9c3-130">-ResourceId</span></span>
<span data-ttu-id="4a9c3-131">Pobiera lub ustawia identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="4a9c3-131">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a9c3-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4a9c3-132">-Confirm</span></span>
<span data-ttu-id="4a9c3-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a9c3-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a9c3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a9c3-134">-WhatIf</span></span>
<span data-ttu-id="4a9c3-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a9c3-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a9c3-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4a9c3-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a9c3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a9c3-137">CommonParameters</span></span>
<span data-ttu-id="4a9c3-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a9c3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a9c3-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a9c3-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a9c3-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a9c3-140">INPUTS</span></span>

### <span data-ttu-id="4a9c3-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4a9c3-141">None</span></span>

## <span data-ttu-id="4a9c3-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4a9c3-142">OUTPUTS</span></span>

### <span data-ttu-id="4a9c3-143">Microsoft. Azure. Management. HDInsight. MODELES. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="4a9c3-143">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="4a9c3-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4a9c3-144">NOTES</span></span>

## <span data-ttu-id="4a9c3-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a9c3-145">RELATED LINKS</span></span>