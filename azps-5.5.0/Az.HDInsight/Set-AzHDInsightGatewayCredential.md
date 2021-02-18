---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightgatewaycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
ms.openlocfilehash: f3997247c9a32fa9066e17dff3a09f2bd65a80d5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241378"
---
# <span data-ttu-id="01dff-101">Set-AzHDInsightGatewayCredential</span><span class="sxs-lookup"><span data-stu-id="01dff-101">Set-AzHDInsightGatewayCredential</span></span>

## <span data-ttu-id="01dff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01dff-102">SYNOPSIS</span></span>
<span data-ttu-id="01dff-103">Ustawia poświadczenia HTTP bramy dla klastru usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="01dff-103">Sets the gateway HTTP credentials of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="01dff-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="01dff-104">SYNTAX</span></span>

### <span data-ttu-id="01dff-105">SetByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="01dff-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightGatewayCredential [-Name] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01dff-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01dff-106">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -InputObject <AzureHDInsightCluster> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01dff-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="01dff-107">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01dff-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="01dff-108">DESCRIPTION</span></span>
<span data-ttu-id="01dff-109">Polecenie **cmdlet Set-AzHDInsightGatewayCredential** ustawia poświadczenia bramy klastru usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="01dff-109">The **Set-AzHDInsightGatewayCredential** cmdlet sets gateway credential of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="01dff-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="01dff-110">EXAMPLES</span></span>

### <span data-ttu-id="01dff-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="01dff-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Set-AzHDInsightGatewayCredential `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="01dff-112">To polecenie ustawia poświadczenia bramy klastru o nazwie Twoja-hadoop-001 według zestawu parametrów nazwy.</span><span class="sxs-lookup"><span data-stu-id="01dff-112">This command sets gateway credential of the cluster named your-hadoop-001 by name parameter set.</span></span>

### <span data-ttu-id="01dff-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="01dff-113">Example 2</span></span>
```powershell
PS C:\> Set-AzHDInsightGatewayCredential `
            -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.HDInsight/clusters/your-hadoop-001" `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="01dff-114">To polecenie ustawia poświadczenia bramy klastru o nazwie Twoja-hadoop-001 przez zestaw parametrów ResourceId.</span><span class="sxs-lookup"><span data-stu-id="01dff-114">This command sets gateway credential of the cluster named your-hadoop-001 by ResourceId parameter set.</span></span>

### <span data-ttu-id="01dff-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="01dff-115">Example 3</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Get-AzHDInsightCluster -ClusterName $clusterName | Set-AzHDInsightGatewayCredential `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="01dff-116">To polecenie ustawia poświadczenia bramy klastru o nazwie Twoja-hadoop-001 przez zestaw parametrów InputObject.</span><span class="sxs-lookup"><span data-stu-id="01dff-116">This command sets gateway credential of the cluster named your-hadoop-001 by InputObject parameter set.</span></span>

## <span data-ttu-id="01dff-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01dff-117">PARAMETERS</span></span>

### <span data-ttu-id="01dff-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="01dff-118">-AsJob</span></span>
<span data-ttu-id="01dff-119">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="01dff-119">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="01dff-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01dff-120">-DefaultProfile</span></span>
<span data-ttu-id="01dff-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="01dff-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01dff-122">- HttpCredential</span><span class="sxs-lookup"><span data-stu-id="01dff-122">-HttpCredential</span></span>
<span data-ttu-id="01dff-123">Pobiera lub ustawia logowanie użytkownika klastra.</span><span class="sxs-lookup"><span data-stu-id="01dff-123">Gets or sets the login for the cluster's user.</span></span>

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

### <span data-ttu-id="01dff-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01dff-124">-InputObject</span></span>
<span data-ttu-id="01dff-125">Pobiera lub ustawia obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="01dff-125">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="01dff-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="01dff-126">-Name</span></span>
<span data-ttu-id="01dff-127">Pobiera lub ustawia nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="01dff-127">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01dff-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01dff-128">-ResourceGroupName</span></span>
<span data-ttu-id="01dff-129">Pobiera lub ustawia nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="01dff-129">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01dff-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01dff-130">-ResourceId</span></span>
<span data-ttu-id="01dff-131">Pobiera lub ustawia identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="01dff-131">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="01dff-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="01dff-132">-Confirm</span></span>
<span data-ttu-id="01dff-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="01dff-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01dff-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01dff-134">-WhatIf</span></span>
<span data-ttu-id="01dff-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01dff-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01dff-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="01dff-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01dff-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01dff-137">CommonParameters</span></span>
<span data-ttu-id="01dff-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01dff-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01dff-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01dff-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01dff-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01dff-140">INPUTS</span></span>

### <span data-ttu-id="01dff-141">Brak</span><span class="sxs-lookup"><span data-stu-id="01dff-141">None</span></span>

## <span data-ttu-id="01dff-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01dff-142">OUTPUTS</span></span>

### <span data-ttu-id="01dff-143">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightGatewaySettings</span><span class="sxs-lookup"><span data-stu-id="01dff-143">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightGatewaySettings</span></span>

## <span data-ttu-id="01dff-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="01dff-144">NOTES</span></span>

## <span data-ttu-id="01dff-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01dff-145">RELATED LINKS</span></span>
