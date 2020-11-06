---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/set-azurermservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
ms.openlocfilehash: 8a675355806a8b4579abcea965a5e0e0b8128207
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551568"
---
# <span data-ttu-id="a6b3d-101">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="a6b3d-101">Set-AzureRmServiceFabricUpgradeType</span></span>

## <span data-ttu-id="a6b3d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a6b3d-102">SYNOPSIS</span></span>
<span data-ttu-id="a6b3d-103">Zmienianie typu uaktualnienia sieci szkieletowej usług dla klastra.</span><span class="sxs-lookup"><span data-stu-id="a6b3d-103">Change the Service Fabric upgrade type of the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6b3d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a6b3d-104">SYNTAX</span></span>

### <span data-ttu-id="a6b3d-105">Automatyczne</span><span class="sxs-lookup"><span data-stu-id="a6b3d-105">Automatic</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a6b3d-106">Ręcznie</span><span class="sxs-lookup"><span data-stu-id="a6b3d-106">Manual</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6b3d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a6b3d-107">DESCRIPTION</span></span>
<span data-ttu-id="a6b3d-108">Funkcja **Set-AzureRmServiceFabricUpgradeType** umożliwia ustawienie typu uaktualnienia na automatyczny lub ręczny z określoną wersją kodu sieci szkieletowej usługi.</span><span class="sxs-lookup"><span data-stu-id="a6b3d-108">Use **Set-AzureRmServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="a6b3d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a6b3d-109">EXAMPLES</span></span>

### <span data-ttu-id="a6b3d-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a6b3d-110">Example 1</span></span>
```
PS c:> Set-AzureRmServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="a6b3d-111">To polecenie spowoduje ustawienie trybu uaktualniania klastra na wartość automatycznie.</span><span class="sxs-lookup"><span data-stu-id="a6b3d-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="a6b3d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a6b3d-112">PARAMETERS</span></span>

### <span data-ttu-id="a6b3d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6b3d-113">-DefaultProfile</span></span>
<span data-ttu-id="a6b3d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a6b3d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6b3d-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a6b3d-115">-Name</span></span>
<span data-ttu-id="a6b3d-116">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="a6b3d-116">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6b3d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6b3d-117">-ResourceGroupName</span></span>
<span data-ttu-id="a6b3d-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a6b3d-118">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6b3d-119">-Upgrademode</span><span class="sxs-lookup"><span data-stu-id="a6b3d-119">-UpgradeMode</span></span>
<span data-ttu-id="a6b3d-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="a6b3d-120">ClusterUpgradeMode</span></span>

```yaml
Type: ClusterUpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6b3d-121">-Version</span><span class="sxs-lookup"><span data-stu-id="a6b3d-121">-Version</span></span>
<span data-ttu-id="a6b3d-122">Wersja kodu klastra.</span><span class="sxs-lookup"><span data-stu-id="a6b3d-122">Cluster code version.</span></span>

```yaml
Type: String
Parameter Sets: Manual
Aliases: ClusterCodeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6b3d-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a6b3d-123">-Confirm</span></span>
<span data-ttu-id="a6b3d-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6b3d-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6b3d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6b3d-125">-WhatIf</span></span>
<span data-ttu-id="a6b3d-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6b3d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6b3d-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a6b3d-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6b3d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6b3d-128">CommonParameters</span></span>
<span data-ttu-id="a6b3d-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6b3d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6b3d-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6b3d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6b3d-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6b3d-131">INPUTS</span></span>

### <span data-ttu-id="a6b3d-132">Microsoft. Azure. Commands. servicefabric. MODELES. ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="a6b3d-132">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>
<span data-ttu-id="a6b3d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a6b3d-133">System.String</span></span>

## <span data-ttu-id="a6b3d-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a6b3d-134">OUTPUTS</span></span>

### <span data-ttu-id="a6b3d-135">Microsoft. Azure. Commands. servicefabric. MODELES. PsCluster</span><span class="sxs-lookup"><span data-stu-id="a6b3d-135">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="a6b3d-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a6b3d-136">NOTES</span></span>

## <span data-ttu-id="a6b3d-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6b3d-137">RELATED LINKS</span></span>

