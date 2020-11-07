---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
ms.openlocfilehash: 161b97ffd032c8a6f7aca6b40c719a45b7e6a935
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871176"
---
# <span data-ttu-id="66cb7-101">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="66cb7-101">Remove-AzRouteTable</span></span>

## <span data-ttu-id="66cb7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="66cb7-102">SYNOPSIS</span></span>
<span data-ttu-id="66cb7-103">Usuwa tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="66cb7-103">Removes a route table.</span></span>

## <span data-ttu-id="66cb7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="66cb7-104">SYNTAX</span></span>

```
Remove-AzRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66cb7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="66cb7-105">DESCRIPTION</span></span>
<span data-ttu-id="66cb7-106">Polecenie cmdlet **Remove-AzRouteTable** usuwa tabelę routingu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="66cb7-106">The **Remove-AzRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="66cb7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="66cb7-107">EXAMPLES</span></span>

### <span data-ttu-id="66cb7-108">Przykład 1: Usuwanie tabeli tras</span><span class="sxs-lookup"><span data-stu-id="66cb7-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="66cb7-109">To polecenie usuwa tabelę routingu o nazwie RouteTable01 w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="66cb7-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="66cb7-110">Polecenie cmdlet monituje o potwierdzenie przed usunięciem tabeli.</span><span class="sxs-lookup"><span data-stu-id="66cb7-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="66cb7-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="66cb7-111">PARAMETERS</span></span>

### <span data-ttu-id="66cb7-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66cb7-112">-AsJob</span></span>
<span data-ttu-id="66cb7-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="66cb7-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66cb7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66cb7-114">-DefaultProfile</span></span>
<span data-ttu-id="66cb7-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="66cb7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66cb7-116">-Force</span><span class="sxs-lookup"><span data-stu-id="66cb7-116">-Force</span></span>
<span data-ttu-id="66cb7-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="66cb7-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="66cb7-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="66cb7-118">-Name</span></span>
<span data-ttu-id="66cb7-119">Określa nazwę tabeli routingu, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66cb7-119">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="66cb7-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66cb7-120">-PassThru</span></span>
<span data-ttu-id="66cb7-121">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="66cb7-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="66cb7-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="66cb7-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="66cb7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66cb7-123">-ResourceGroupName</span></span>
<span data-ttu-id="66cb7-124">Określa nazwę grupy zasobów zawierającej tabelę tras, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66cb7-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="66cb7-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="66cb7-125">-Confirm</span></span>
<span data-ttu-id="66cb7-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66cb7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66cb7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66cb7-127">-WhatIf</span></span>
<span data-ttu-id="66cb7-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66cb7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66cb7-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="66cb7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66cb7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66cb7-130">CommonParameters</span></span>
<span data-ttu-id="66cb7-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66cb7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66cb7-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66cb7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66cb7-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66cb7-133">INPUTS</span></span>

### <span data-ttu-id="66cb7-134">System. String</span><span class="sxs-lookup"><span data-stu-id="66cb7-134">System.String</span></span>

## <span data-ttu-id="66cb7-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="66cb7-135">OUTPUTS</span></span>

### <span data-ttu-id="66cb7-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="66cb7-136">System.Boolean</span></span>

## <span data-ttu-id="66cb7-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="66cb7-137">NOTES</span></span>

## <span data-ttu-id="66cb7-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="66cb7-138">RELATED LINKS</span></span>

[<span data-ttu-id="66cb7-139">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="66cb7-139">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="66cb7-140">Nowe — AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="66cb7-140">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="66cb7-141">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="66cb7-141">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


