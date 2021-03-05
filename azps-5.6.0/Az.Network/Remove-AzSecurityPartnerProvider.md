---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
ms.openlocfilehash: 3fda360369615c28647769e6bc5aeb0af71e0e35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006170"
---
# <span data-ttu-id="c550f-101">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="c550f-101">Remove-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="c550f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c550f-102">SYNOPSIS</span></span>
<span data-ttu-id="c550f-103">Usuwa narzędzie Azure SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="c550f-103">Deletes an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="c550f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c550f-104">SYNTAX</span></span>

### <span data-ttu-id="c550f-105">SecurityPartnerProviderNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c550f-105">SecurityPartnerProviderNameParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c550f-106">SecurityPartnerProviderInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c550f-106">SecurityPartnerProviderInputObjectParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c550f-107">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c550f-107">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c550f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c550f-108">DESCRIPTION</span></span>
<span data-ttu-id="c550f-109">Polecenie **cmdlet Remove-AzSecurityPartnerProvider** usuwa element Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="c550f-109">The **Remove-AzSecurityPartnerProvider** cmdlet deletes an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="c550f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c550f-110">EXAMPLES</span></span>

### <span data-ttu-id="c550f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c550f-111">Example 1</span></span>
```powershell
Remove-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```

## <span data-ttu-id="c550f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c550f-112">PARAMETERS</span></span>

### <span data-ttu-id="c550f-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="c550f-113">-AsJob</span></span>
<span data-ttu-id="c550f-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c550f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c550f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c550f-115">-DefaultProfile</span></span>
<span data-ttu-id="c550f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c550f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c550f-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="c550f-117">-Force</span></span>
<span data-ttu-id="c550f-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c550f-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c550f-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c550f-119">-Name</span></span>
<span data-ttu-id="c550f-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="c550f-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c550f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c550f-121">-PassThru</span></span>
<span data-ttu-id="c550f-122">Zwraca obiekt reprezentujący element, na którym jest wykonywana ta operacja.</span><span class="sxs-lookup"><span data-stu-id="c550f-122">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="c550f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c550f-123">-ResourceGroupName</span></span>
<span data-ttu-id="c550f-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c550f-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c550f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c550f-125">-ResourceId</span></span>
<span data-ttu-id="c550f-126">Identyfikator zasobu securityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="c550f-126">The securityPartnerProvider resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c550f-127">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="c550f-127">-SecurityPartnerProvider</span></span>
<span data-ttu-id="c550f-128">Obiekt wejściowy securityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="c550f-128">The securityPartnerProvider input object.</span></span>

```yaml
Type: PSSecurityPartnerProvider
Parameter Sets: SecurityPartnerProviderInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c550f-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c550f-129">-Confirm</span></span>
<span data-ttu-id="c550f-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c550f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c550f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c550f-131">-WhatIf</span></span>
<span data-ttu-id="c550f-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c550f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c550f-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c550f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c550f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c550f-134">CommonParameters</span></span>
<span data-ttu-id="c550f-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c550f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c550f-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c550f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c550f-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c550f-137">INPUTS</span></span>

### <span data-ttu-id="c550f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c550f-138">System.String</span></span>

### <span data-ttu-id="c550f-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="c550f-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="c550f-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c550f-140">OUTPUTS</span></span>

### <span data-ttu-id="c550f-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c550f-141">System.Boolean</span></span>

## <span data-ttu-id="c550f-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c550f-142">NOTES</span></span>

## <span data-ttu-id="c550f-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c550f-143">RELATED LINKS</span></span>
