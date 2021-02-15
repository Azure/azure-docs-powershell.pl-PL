---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
ms.openlocfilehash: 346bb9cb073488d0112ea08db22fb1f6c387bac9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197803"
---
# <span data-ttu-id="3b00c-101">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="3b00c-101">Set-AzServiceFabricUpgradeType</span></span>

## <span data-ttu-id="3b00c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b00c-102">SYNOPSIS</span></span>
<span data-ttu-id="3b00c-103">Zmienianie typu uaktualniania sieci szkieletów usług w klastrze.</span><span class="sxs-lookup"><span data-stu-id="3b00c-103">Change the Service Fabric upgrade type of the cluster.</span></span>

## <span data-ttu-id="3b00c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3b00c-104">SYNTAX</span></span>

### <span data-ttu-id="3b00c-105">Automatyczne</span><span class="sxs-lookup"><span data-stu-id="3b00c-105">Automatic</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b00c-106">Ręcznie</span><span class="sxs-lookup"><span data-stu-id="3b00c-106">Manual</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b00c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="3b00c-107">DESCRIPTION</span></span>
<span data-ttu-id="3b00c-108">Użyj **set-AzServiceFabricUpgradeType,** aby ustawić typ uaktualnienia do automatycznego lub ręcznego z określoną wersją kodu service Fabric.</span><span class="sxs-lookup"><span data-stu-id="3b00c-108">Use **Set-AzServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="3b00c-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3b00c-109">EXAMPLES</span></span>

### <span data-ttu-id="3b00c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3b00c-110">Example 1</span></span>
```
PS c:> Set-AzServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="3b00c-111">To polecenie ustawi tryb uaktualniania klastrów na automatyczny.</span><span class="sxs-lookup"><span data-stu-id="3b00c-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="3b00c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b00c-112">PARAMETERS</span></span>

### <span data-ttu-id="3b00c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b00c-113">-DefaultProfile</span></span>
<span data-ttu-id="3b00c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3b00c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b00c-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3b00c-115">-Name</span></span>
<span data-ttu-id="3b00c-116">Określanie nazwy klastra</span><span class="sxs-lookup"><span data-stu-id="3b00c-116">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b00c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b00c-117">-ResourceGroupName</span></span>
<span data-ttu-id="3b00c-118">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3b00c-118">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b00c-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="3b00c-119">-UpgradeMode</span></span>
<span data-ttu-id="3b00c-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="3b00c-120">ClusterUpgradeMode</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b00c-121">— Wersja</span><span class="sxs-lookup"><span data-stu-id="3b00c-121">-Version</span></span>
<span data-ttu-id="3b00c-122">Wersja kodu klastrowego</span><span class="sxs-lookup"><span data-stu-id="3b00c-122">Cluster code version</span></span>

```yaml
Type: System.String
Parameter Sets: Manual
Aliases: ClusterCodeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b00c-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3b00c-123">-Confirm</span></span>
<span data-ttu-id="3b00c-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3b00c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b00c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b00c-125">-WhatIf</span></span>
<span data-ttu-id="3b00c-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b00c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b00c-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3b00c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b00c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b00c-128">CommonParameters</span></span>
<span data-ttu-id="3b00c-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b00c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b00c-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b00c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b00c-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b00c-131">INPUTS</span></span>

### <span data-ttu-id="3b00c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="3b00c-132">System.String</span></span>

### <span data-ttu-id="3b00c-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="3b00c-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>

## <span data-ttu-id="3b00c-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b00c-134">OUTPUTS</span></span>

### <span data-ttu-id="3b00c-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="3b00c-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="3b00c-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3b00c-136">NOTES</span></span>

## <span data-ttu-id="3b00c-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b00c-137">RELATED LINKS</span></span>
