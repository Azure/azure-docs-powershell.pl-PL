---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
ms.openlocfilehash: 346bb9cb073488d0112ea08db22fb1f6c387bac9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233923"
---
# <span data-ttu-id="e7deb-101">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="e7deb-101">Set-AzServiceFabricUpgradeType</span></span>

## <span data-ttu-id="e7deb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e7deb-102">SYNOPSIS</span></span>
<span data-ttu-id="e7deb-103">Zmienianie typu uaktualnienia sieci szkieletowej usług dla klastra.</span><span class="sxs-lookup"><span data-stu-id="e7deb-103">Change the Service Fabric upgrade type of the cluster.</span></span>

## <span data-ttu-id="e7deb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e7deb-104">SYNTAX</span></span>

### <span data-ttu-id="e7deb-105">Automatyczne</span><span class="sxs-lookup"><span data-stu-id="e7deb-105">Automatic</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7deb-106">Ręcznie</span><span class="sxs-lookup"><span data-stu-id="e7deb-106">Manual</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7deb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e7deb-107">DESCRIPTION</span></span>
<span data-ttu-id="e7deb-108">Funkcja **Set-AzServiceFabricUpgradeType** umożliwia ustawienie typu uaktualnienia na automatyczny lub ręczny z określoną wersją kodu sieci szkieletowej usługi.</span><span class="sxs-lookup"><span data-stu-id="e7deb-108">Use **Set-AzServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="e7deb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e7deb-109">EXAMPLES</span></span>

### <span data-ttu-id="e7deb-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e7deb-110">Example 1</span></span>
```
PS c:> Set-AzServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="e7deb-111">To polecenie spowoduje ustawienie trybu uaktualniania klastra na wartość automatycznie.</span><span class="sxs-lookup"><span data-stu-id="e7deb-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="e7deb-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e7deb-112">PARAMETERS</span></span>

### <span data-ttu-id="e7deb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7deb-113">-DefaultProfile</span></span>
<span data-ttu-id="e7deb-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7deb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7deb-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e7deb-115">-Name</span></span>
<span data-ttu-id="e7deb-116">Określanie nazwy klastra</span><span class="sxs-lookup"><span data-stu-id="e7deb-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="e7deb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7deb-117">-ResourceGroupName</span></span>
<span data-ttu-id="e7deb-118">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e7deb-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="e7deb-119">-Upgrademode</span><span class="sxs-lookup"><span data-stu-id="e7deb-119">-UpgradeMode</span></span>
<span data-ttu-id="e7deb-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="e7deb-120">ClusterUpgradeMode</span></span>

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

### <span data-ttu-id="e7deb-121">-Version</span><span class="sxs-lookup"><span data-stu-id="e7deb-121">-Version</span></span>
<span data-ttu-id="e7deb-122">Wersja kodu klastra</span><span class="sxs-lookup"><span data-stu-id="e7deb-122">Cluster code version</span></span>

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

### <span data-ttu-id="e7deb-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e7deb-123">-Confirm</span></span>
<span data-ttu-id="e7deb-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7deb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7deb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7deb-125">-WhatIf</span></span>
<span data-ttu-id="e7deb-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7deb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7deb-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e7deb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7deb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7deb-128">CommonParameters</span></span>
<span data-ttu-id="e7deb-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7deb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7deb-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7deb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7deb-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7deb-131">INPUTS</span></span>

### <span data-ttu-id="e7deb-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e7deb-132">System.String</span></span>

### <span data-ttu-id="e7deb-133">Microsoft. Azure. Commands. servicefabric. MODELES. ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="e7deb-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>

## <span data-ttu-id="e7deb-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e7deb-134">OUTPUTS</span></span>

### <span data-ttu-id="e7deb-135">Microsoft. Azure. Commands. servicefabric. MODELES. PSCluster</span><span class="sxs-lookup"><span data-stu-id="e7deb-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="e7deb-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e7deb-136">NOTES</span></span>

## <span data-ttu-id="e7deb-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7deb-137">RELATED LINKS</span></span>
