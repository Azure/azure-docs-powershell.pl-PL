---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteTable.md
ms.openlocfilehash: ddd1ab1ce748def345604447988d0fc53b5989fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718640"
---
# <span data-ttu-id="e7bba-101">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="e7bba-101">Remove-AzureRmRouteTable</span></span>

## <span data-ttu-id="e7bba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e7bba-102">SYNOPSIS</span></span>
<span data-ttu-id="e7bba-103">Usuwa tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="e7bba-103">Removes a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7bba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e7bba-104">SYNTAX</span></span>

```
Remove-AzureRmRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7bba-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e7bba-105">DESCRIPTION</span></span>
<span data-ttu-id="e7bba-106">Polecenie cmdlet **Remove-AzureRmRouteTable** usuwa tabelę routingu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e7bba-106">The **Remove-AzureRmRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="e7bba-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e7bba-107">EXAMPLES</span></span>

### <span data-ttu-id="e7bba-108">Przykład 1: Usuwanie tabeli tras</span><span class="sxs-lookup"><span data-stu-id="e7bba-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzureRmRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="e7bba-109">To polecenie usuwa tabelę routingu o nazwie RouteTable01 w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e7bba-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="e7bba-110">Polecenie cmdlet monituje o potwierdzenie przed usunięciem tabeli.</span><span class="sxs-lookup"><span data-stu-id="e7bba-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="e7bba-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e7bba-111">PARAMETERS</span></span>

### <span data-ttu-id="e7bba-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7bba-112">-AsJob</span></span>
<span data-ttu-id="e7bba-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e7bba-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e7bba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7bba-114">-DefaultProfile</span></span>
<span data-ttu-id="e7bba-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7bba-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7bba-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e7bba-116">-Force</span></span>
<span data-ttu-id="e7bba-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e7bba-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e7bba-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e7bba-118">-Name</span></span>
<span data-ttu-id="e7bba-119">Określa nazwę tabeli routingu, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7bba-119">Specifies the name of the route table that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bba-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7bba-120">-PassThru</span></span>
<span data-ttu-id="e7bba-121">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="e7bba-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e7bba-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="e7bba-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e7bba-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7bba-123">-ResourceGroupName</span></span>
<span data-ttu-id="e7bba-124">Określa nazwę grupy zasobów zawierającej tabelę tras, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7bba-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bba-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e7bba-125">-Confirm</span></span>
<span data-ttu-id="e7bba-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7bba-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7bba-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7bba-127">-WhatIf</span></span>
<span data-ttu-id="e7bba-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7bba-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7bba-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e7bba-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7bba-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7bba-130">CommonParameters</span></span>
<span data-ttu-id="e7bba-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7bba-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7bba-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7bba-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7bba-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7bba-133">INPUTS</span></span>

### <span data-ttu-id="e7bba-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e7bba-134">None</span></span>
<span data-ttu-id="e7bba-135">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e7bba-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e7bba-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e7bba-136">OUTPUTS</span></span>

## <span data-ttu-id="e7bba-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e7bba-137">NOTES</span></span>

## <span data-ttu-id="e7bba-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7bba-138">RELATED LINKS</span></span>

[<span data-ttu-id="e7bba-139">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="e7bba-139">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="e7bba-140">Nowe — AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="e7bba-140">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="e7bba-141">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="e7bba-141">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


