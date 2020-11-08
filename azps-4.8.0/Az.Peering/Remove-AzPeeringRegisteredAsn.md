---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d43fe033b58ba6295728bc0c21ddb1d853587b59
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223684"
---
# <span data-ttu-id="058a5-101">Remove-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="058a5-101">Remove-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="058a5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="058a5-102">SYNOPSIS</span></span>
<span data-ttu-id="058a5-103">Usuwanie lub usuwanie zarejestrowanego konta ASN z nadrzędnego zasobu równorzędnego.</span><span class="sxs-lookup"><span data-stu-id="058a5-103">Delete or remove a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="058a5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="058a5-104">SYNTAX</span></span>

### <span data-ttu-id="058a5-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="058a5-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="058a5-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="058a5-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredAsn -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="058a5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="058a5-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="058a5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="058a5-108">DESCRIPTION</span></span>
<span data-ttu-id="058a5-109">Umożliwia usunięcie zarejestrowanego konta ASN z nadrzędnego zasobu równorzędnego.</span><span class="sxs-lookup"><span data-stu-id="058a5-109">Allows the removal of registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="058a5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="058a5-110">EXAMPLES</span></span>

### <span data-ttu-id="058a5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="058a5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredAsn -ResourceId $resourceId
```

<span data-ttu-id="058a5-112">Usuwanie rejestru ASN o identyfikatorze zasobu.</span><span class="sxs-lookup"><span data-stu-id="058a5-112">Remove a registerd ASN by resource id.</span></span>

## <span data-ttu-id="058a5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="058a5-113">PARAMETERS</span></span>

### <span data-ttu-id="058a5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="058a5-114">-AsJob</span></span>
<span data-ttu-id="058a5-115">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="058a5-115">Run in the background.</span></span>

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

### <span data-ttu-id="058a5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="058a5-116">-DefaultProfile</span></span>
<span data-ttu-id="058a5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="058a5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="058a5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="058a5-118">-Force</span></span>
<span data-ttu-id="058a5-119">Wymuszanie ukończenia operacji</span><span class="sxs-lookup"><span data-stu-id="058a5-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="058a5-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="058a5-120">-InputObject</span></span>
<span data-ttu-id="058a5-121">Używanie Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="058a5-121">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="058a5-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="058a5-122">-Name</span></span>
<span data-ttu-id="058a5-123">Nazwa zarejestrowanego konta ASN</span><span class="sxs-lookup"><span data-stu-id="058a5-123">The name of the registered ASN</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="058a5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="058a5-124">-PassThru</span></span>
<span data-ttu-id="058a5-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="058a5-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="058a5-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="058a5-126">-PeeringName</span></span>
<span data-ttu-id="058a5-127">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="058a5-127">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="058a5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="058a5-128">-ResourceGroupName</span></span>
<span data-ttu-id="058a5-129">Tworzenie lub używanie istniejącej nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="058a5-129">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="058a5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="058a5-130">-ResourceId</span></span>
<span data-ttu-id="058a5-131">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="058a5-131">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="058a5-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="058a5-132">-Confirm</span></span>
<span data-ttu-id="058a5-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="058a5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="058a5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="058a5-134">-WhatIf</span></span>
<span data-ttu-id="058a5-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="058a5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="058a5-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="058a5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="058a5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="058a5-137">CommonParameters</span></span>
<span data-ttu-id="058a5-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="058a5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="058a5-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="058a5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="058a5-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="058a5-140">INPUTS</span></span>

### <span data-ttu-id="058a5-141">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="058a5-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="058a5-142">System. String</span><span class="sxs-lookup"><span data-stu-id="058a5-142">System.String</span></span>

## <span data-ttu-id="058a5-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="058a5-143">OUTPUTS</span></span>

### <span data-ttu-id="058a5-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="058a5-144">System.Boolean</span></span>

## <span data-ttu-id="058a5-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="058a5-145">NOTES</span></span>

## <span data-ttu-id="058a5-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="058a5-146">RELATED LINKS</span></span>
