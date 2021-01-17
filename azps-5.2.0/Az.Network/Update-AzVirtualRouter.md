---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
ms.openlocfilehash: d7f52ded01ce5b785c1e935ba8d3ebf4b1c0a5fa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350746"
---
# <span data-ttu-id="ed8aa-101">Update-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="ed8aa-101">Update-AzVirtualRouter</span></span>

## <span data-ttu-id="ed8aa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ed8aa-102">SYNOPSIS</span></span>
<span data-ttu-id="ed8aa-103">Umożliwia zaktualizowanie routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="ed8aa-103">Updates a Virtual Router.</span></span> 

## <span data-ttu-id="ed8aa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ed8aa-104">SYNTAX</span></span>

### <span data-ttu-id="ed8aa-105">VirtualRouterNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ed8aa-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-AllowBranchToBranchTraffic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed8aa-106">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed8aa-106">VirtualRouterResourceIdParameterSet</span></span>
```
Update-AzVirtualRouter [-AllowBranchToBranchTraffic] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed8aa-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ed8aa-107">DESCRIPTION</span></span>
<span data-ttu-id="ed8aa-108">Umożliwia zaktualizowanie routera wirtualnego w celu włączenia lub wyłączenia gałęzi do ruchu w oddziale.</span><span class="sxs-lookup"><span data-stu-id="ed8aa-108">Updates Virtual Router to enable or disable branch to branch traffic.</span></span>

## <span data-ttu-id="ed8aa-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ed8aa-109">EXAMPLES</span></span>

### <span data-ttu-id="ed8aa-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ed8aa-110">Example 1</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName -AllowBranchToBranchTraffic
```

<span data-ttu-id="ed8aa-111">Umożliwia zaktualizowanie routera wirtualnego w celu zezwolenia na odgałęzienie do ruchu w oddziale</span><span class="sxs-lookup"><span data-stu-id="ed8aa-111">Updates the Virtual Router to allow branch to branch traffic</span></span>

### <span data-ttu-id="ed8aa-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ed8aa-112">Example 2</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName
```

<span data-ttu-id="ed8aa-113">Umożliwia zaktualizowanie routera wirtualnego w celu zablokowania ruchu odgałęzienia</span><span class="sxs-lookup"><span data-stu-id="ed8aa-113">Updates the Virtual Router to block branch to branch traffic</span></span>

## <span data-ttu-id="ed8aa-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ed8aa-114">PARAMETERS</span></span>

### <span data-ttu-id="ed8aa-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="ed8aa-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="ed8aa-116">Flaga zezwalająca na odgałęzienie do ruchu w oddziale dla routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="ed8aa-116">Flag to allow branch to branch traffic for virtual router.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed8aa-117">-DefaultProfile</span></span>
<span data-ttu-id="ed8aa-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed8aa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8aa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed8aa-119">-ResourceGroupName</span></span>
<span data-ttu-id="ed8aa-120">Nazwa grupy zasobów routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="ed8aa-120">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8aa-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed8aa-121">-ResourceId</span></span>
<span data-ttu-id="ed8aa-122">Identyfikator zasobu routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="ed8aa-122">ResourceId of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8aa-123">-Routername</span><span class="sxs-lookup"><span data-stu-id="ed8aa-123">-RouterName</span></span>
<span data-ttu-id="ed8aa-124">Nazwa routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="ed8aa-124">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8aa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed8aa-125">CommonParameters</span></span>
<span data-ttu-id="ed8aa-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed8aa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed8aa-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed8aa-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed8aa-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed8aa-128">INPUTS</span></span>

### <span data-ttu-id="ed8aa-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ed8aa-129">System.String</span></span>

## <span data-ttu-id="ed8aa-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ed8aa-130">OUTPUTS</span></span>

### <span data-ttu-id="ed8aa-131">Microsoft. Azure. Commands. Network. models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="ed8aa-131">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="ed8aa-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ed8aa-132">NOTES</span></span>

## <span data-ttu-id="ed8aa-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed8aa-133">RELATED LINKS</span></span>
