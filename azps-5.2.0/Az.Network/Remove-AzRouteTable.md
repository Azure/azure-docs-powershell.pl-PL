---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
ms.openlocfilehash: 8c899d975669404045aa40bee45ad287a26f8749
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365304"
---
# <span data-ttu-id="0a170-101">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="0a170-101">Remove-AzRouteTable</span></span>

## <span data-ttu-id="0a170-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0a170-102">SYNOPSIS</span></span>
<span data-ttu-id="0a170-103">Usuwa tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="0a170-103">Removes a route table.</span></span>

## <span data-ttu-id="0a170-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0a170-104">SYNTAX</span></span>

```
Remove-AzRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a170-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0a170-105">DESCRIPTION</span></span>
<span data-ttu-id="0a170-106">Polecenie cmdlet **Remove-AzRouteTable** usuwa tabelę routingu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0a170-106">The **Remove-AzRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="0a170-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0a170-107">EXAMPLES</span></span>

### <span data-ttu-id="0a170-108">Przykład 1: Usuwanie tabeli tras</span><span class="sxs-lookup"><span data-stu-id="0a170-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="0a170-109">To polecenie usuwa tabelę routingu o nazwie RouteTable01 w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0a170-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="0a170-110">Polecenie cmdlet monituje o potwierdzenie przed usunięciem tabeli.</span><span class="sxs-lookup"><span data-stu-id="0a170-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="0a170-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0a170-111">PARAMETERS</span></span>

### <span data-ttu-id="0a170-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a170-112">-AsJob</span></span>
<span data-ttu-id="0a170-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0a170-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a170-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a170-114">-DefaultProfile</span></span>
<span data-ttu-id="0a170-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0a170-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a170-116">-Force</span><span class="sxs-lookup"><span data-stu-id="0a170-116">-Force</span></span>
<span data-ttu-id="0a170-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0a170-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0a170-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0a170-118">-Name</span></span>
<span data-ttu-id="0a170-119">Określa nazwę tabeli routingu, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a170-119">Specifies the name of the route table that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a170-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a170-120">-PassThru</span></span>
<span data-ttu-id="0a170-121">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="0a170-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0a170-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="0a170-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0a170-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a170-123">-ResourceGroupName</span></span>
<span data-ttu-id="0a170-124">Określa nazwę grupy zasobów zawierającej tabelę tras, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a170-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a170-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0a170-125">-Confirm</span></span>
<span data-ttu-id="0a170-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a170-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a170-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a170-127">-WhatIf</span></span>
<span data-ttu-id="0a170-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a170-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a170-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0a170-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a170-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a170-130">CommonParameters</span></span>
<span data-ttu-id="0a170-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a170-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a170-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a170-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a170-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a170-133">INPUTS</span></span>

### <span data-ttu-id="0a170-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0a170-134">System.String</span></span>

## <span data-ttu-id="0a170-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0a170-135">OUTPUTS</span></span>

### <span data-ttu-id="0a170-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0a170-136">System.Boolean</span></span>

## <span data-ttu-id="0a170-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0a170-137">NOTES</span></span>

## <span data-ttu-id="0a170-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0a170-138">RELATED LINKS</span></span>

[<span data-ttu-id="0a170-139">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="0a170-139">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="0a170-140">Nowe — AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="0a170-140">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="0a170-141">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="0a170-141">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


