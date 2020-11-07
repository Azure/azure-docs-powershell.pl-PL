---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpPrefix.md
ms.openlocfilehash: e361e4d3c4daec88ddb35fa7973b65f630dcc390
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718801"
---
# <span data-ttu-id="be1aa-101">Remove-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="be1aa-101">Remove-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="be1aa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="be1aa-102">SYNOPSIS</span></span>
<span data-ttu-id="be1aa-103">Usuwa publiczny prefiks IP</span><span class="sxs-lookup"><span data-stu-id="be1aa-103">Removes a public IP prefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be1aa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="be1aa-104">SYNTAX</span></span>

### <span data-ttu-id="be1aa-105">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="be1aa-105">RemoveByNameParameterSet</span></span>
```
Remove-AzureRmPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be1aa-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="be1aa-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzureRmPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be1aa-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be1aa-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzureRmPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be1aa-108">Opis</span><span class="sxs-lookup"><span data-stu-id="be1aa-108">DESCRIPTION</span></span>
<span data-ttu-id="be1aa-109">Polecenie cmdlet \* \* Remove-AzureRmPublicIpPrefix usuwa publiczny prefiks IP usługi Azure, dopóki nie zostaną przydzielone żadne publiczne adresy IP.</span><span class="sxs-lookup"><span data-stu-id="be1aa-109">The \*\*Remove-AzureRmPublicIpPrefix cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="be1aa-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="be1aa-110">EXAMPLES</span></span>

### <span data-ttu-id="be1aa-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="be1aa-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="be1aa-112">Usuwa publiczny prefiks IP z nazwą $prefixName z grupy zasobów $rgName</span><span class="sxs-lookup"><span data-stu-id="be1aa-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="be1aa-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="be1aa-113">PARAMETERS</span></span>

### <span data-ttu-id="be1aa-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be1aa-114">-AsJob</span></span>
<span data-ttu-id="be1aa-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="be1aa-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="be1aa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be1aa-116">-DefaultProfile</span></span>
<span data-ttu-id="be1aa-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="be1aa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be1aa-118">-Force</span><span class="sxs-lookup"><span data-stu-id="be1aa-118">-Force</span></span>
<span data-ttu-id="be1aa-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="be1aa-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="be1aa-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="be1aa-120">-InputObject</span></span>
<span data-ttu-id="be1aa-121">Obiekt PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="be1aa-121">A PublicIpPrefix object</span></span>

```yaml
Type: PSPublicIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be1aa-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="be1aa-122">-Name</span></span>
<span data-ttu-id="be1aa-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="be1aa-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be1aa-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be1aa-124">-PassThru</span></span>
<span data-ttu-id="be1aa-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="be1aa-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="be1aa-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="be1aa-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="be1aa-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be1aa-127">-ResourceGroupName</span></span>
<span data-ttu-id="be1aa-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="be1aa-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be1aa-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be1aa-129">-ResourceId</span></span>
<span data-ttu-id="be1aa-130">Identyfikator zasobu zasobu do usunięcia</span><span class="sxs-lookup"><span data-stu-id="be1aa-130">The resourceId for the resource to remove</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be1aa-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="be1aa-131">-Confirm</span></span>
<span data-ttu-id="be1aa-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be1aa-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be1aa-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be1aa-133">-WhatIf</span></span>
<span data-ttu-id="be1aa-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be1aa-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be1aa-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="be1aa-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be1aa-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be1aa-136">CommonParameters</span></span>
<span data-ttu-id="be1aa-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be1aa-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="be1aa-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be1aa-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be1aa-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be1aa-139">INPUTS</span></span>

### <span data-ttu-id="be1aa-140">System. String</span><span class="sxs-lookup"><span data-stu-id="be1aa-140">System.String</span></span>
<span data-ttu-id="be1aa-141">Microsoft. Azure. Commands. Network. models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="be1aa-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="be1aa-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="be1aa-142">OUTPUTS</span></span>

### <span data-ttu-id="be1aa-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="be1aa-143">System.Object</span></span>

## <span data-ttu-id="be1aa-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="be1aa-144">NOTES</span></span>

## <span data-ttu-id="be1aa-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be1aa-145">RELATED LINKS</span></span>
