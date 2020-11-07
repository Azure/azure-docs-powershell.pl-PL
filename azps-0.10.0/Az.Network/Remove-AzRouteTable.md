---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteTable.md
ms.openlocfilehash: 434d70cbdce08750e69865e59197ebba5fb6e6fb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892925"
---
# <span data-ttu-id="a7620-101">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="a7620-101">Remove-AzRouteTable</span></span>

## <span data-ttu-id="a7620-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a7620-102">SYNOPSIS</span></span>
<span data-ttu-id="a7620-103">Usuwa tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="a7620-103">Removes a route table.</span></span>

## <span data-ttu-id="a7620-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a7620-104">SYNTAX</span></span>

```
Remove-AzRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7620-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a7620-105">DESCRIPTION</span></span>
<span data-ttu-id="a7620-106">Polecenie cmdlet **Remove-AzRouteTable** usuwa tabelę routingu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a7620-106">The **Remove-AzRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="a7620-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a7620-107">EXAMPLES</span></span>

### <span data-ttu-id="a7620-108">Przykład 1: Usuwanie tabeli tras</span><span class="sxs-lookup"><span data-stu-id="a7620-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="a7620-109">To polecenie usuwa tabelę routingu o nazwie RouteTable01 w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a7620-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="a7620-110">Polecenie cmdlet monituje o potwierdzenie przed usunięciem tabeli.</span><span class="sxs-lookup"><span data-stu-id="a7620-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="a7620-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a7620-111">PARAMETERS</span></span>

### <span data-ttu-id="a7620-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7620-112">-AsJob</span></span>
<span data-ttu-id="a7620-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a7620-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a7620-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7620-114">-DefaultProfile</span></span>
<span data-ttu-id="a7620-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a7620-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7620-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a7620-116">-Force</span></span>
<span data-ttu-id="a7620-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a7620-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a7620-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a7620-118">-Name</span></span>
<span data-ttu-id="a7620-119">Określa nazwę tabeli routingu, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7620-119">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a7620-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7620-120">-PassThru</span></span>
<span data-ttu-id="a7620-121">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="a7620-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a7620-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="a7620-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a7620-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7620-123">-ResourceGroupName</span></span>
<span data-ttu-id="a7620-124">Określa nazwę grupy zasobów zawierającej tabelę tras, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7620-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a7620-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a7620-125">-Confirm</span></span>
<span data-ttu-id="a7620-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7620-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7620-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7620-127">-WhatIf</span></span>
<span data-ttu-id="a7620-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7620-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7620-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a7620-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7620-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7620-130">CommonParameters</span></span>
<span data-ttu-id="a7620-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7620-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7620-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7620-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7620-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7620-133">INPUTS</span></span>

## <span data-ttu-id="a7620-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a7620-134">OUTPUTS</span></span>

## <span data-ttu-id="a7620-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a7620-135">NOTES</span></span>

## <span data-ttu-id="a7620-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a7620-136">RELATED LINKS</span></span>

[<span data-ttu-id="a7620-137">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="a7620-137">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="a7620-138">Nowe — AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="a7620-138">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="a7620-139">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="a7620-139">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


