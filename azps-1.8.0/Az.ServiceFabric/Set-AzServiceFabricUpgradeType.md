---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
ms.openlocfilehash: a82bec40d93b33385dfa9aa2b4a5c5d122e59aa2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708067"
---
# <span data-ttu-id="7f7e9-101">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="7f7e9-101">Set-AzServiceFabricUpgradeType</span></span>

## <span data-ttu-id="7f7e9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7f7e9-102">SYNOPSIS</span></span>
<span data-ttu-id="7f7e9-103">Zmienianie typu uaktualnienia sieci szkieletowej usług dla klastra.</span><span class="sxs-lookup"><span data-stu-id="7f7e9-103">Change the Service Fabric upgrade type of the cluster.</span></span>

## <span data-ttu-id="7f7e9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7f7e9-104">SYNTAX</span></span>

### <span data-ttu-id="7f7e9-105">Automatyczne</span><span class="sxs-lookup"><span data-stu-id="7f7e9-105">Automatic</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f7e9-106">Ręcznie</span><span class="sxs-lookup"><span data-stu-id="7f7e9-106">Manual</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f7e9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7f7e9-107">DESCRIPTION</span></span>
<span data-ttu-id="7f7e9-108">Funkcja **Set-AzServiceFabricUpgradeType** umożliwia ustawienie typu uaktualnienia na automatyczny lub ręczny z określoną wersją kodu sieci szkieletowej usługi.</span><span class="sxs-lookup"><span data-stu-id="7f7e9-108">Use **Set-AzServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="7f7e9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7f7e9-109">EXAMPLES</span></span>

### <span data-ttu-id="7f7e9-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7f7e9-110">Example 1</span></span>
```
PS c:> Set-AzServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="7f7e9-111">To polecenie spowoduje ustawienie trybu uaktualniania klastra na wartość automatycznie.</span><span class="sxs-lookup"><span data-stu-id="7f7e9-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="7f7e9-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7f7e9-112">PARAMETERS</span></span>

### <span data-ttu-id="7f7e9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f7e9-113">-DefaultProfile</span></span>
<span data-ttu-id="7f7e9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7f7e9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f7e9-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7f7e9-115">-Name</span></span>
<span data-ttu-id="7f7e9-116">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="7f7e9-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="7f7e9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f7e9-117">-ResourceGroupName</span></span>
<span data-ttu-id="7f7e9-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7f7e9-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7f7e9-119">-Upgrademode</span><span class="sxs-lookup"><span data-stu-id="7f7e9-119">-UpgradeMode</span></span>
<span data-ttu-id="7f7e9-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="7f7e9-120">ClusterUpgradeMode</span></span>

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

### <span data-ttu-id="7f7e9-121">-Version</span><span class="sxs-lookup"><span data-stu-id="7f7e9-121">-Version</span></span>
<span data-ttu-id="7f7e9-122">Wersja kodu klastra.</span><span class="sxs-lookup"><span data-stu-id="7f7e9-122">Cluster code version.</span></span>

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

### <span data-ttu-id="7f7e9-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7f7e9-123">-Confirm</span></span>
<span data-ttu-id="7f7e9-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f7e9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f7e9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f7e9-125">-WhatIf</span></span>
<span data-ttu-id="7f7e9-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f7e9-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f7e9-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7f7e9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f7e9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f7e9-128">CommonParameters</span></span>
<span data-ttu-id="7f7e9-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f7e9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f7e9-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f7e9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f7e9-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f7e9-131">INPUTS</span></span>

### <span data-ttu-id="7f7e9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7f7e9-132">System.String</span></span>

### <span data-ttu-id="7f7e9-133">Microsoft. Azure. Commands. servicefabric. MODELES. ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="7f7e9-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>

## <span data-ttu-id="7f7e9-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7f7e9-134">OUTPUTS</span></span>

### <span data-ttu-id="7f7e9-135">Microsoft. Azure. Commands. servicefabric. MODELES. PSCluster</span><span class="sxs-lookup"><span data-stu-id="7f7e9-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="7f7e9-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7f7e9-136">NOTES</span></span>

## <span data-ttu-id="7f7e9-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f7e9-137">RELATED LINKS</span></span>
