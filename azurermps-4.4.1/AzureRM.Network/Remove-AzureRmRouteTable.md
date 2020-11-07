---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteTable.md
ms.openlocfilehash: 17cd4ab4e60156c1ab4d6dd4357e638ddaf2c5a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717032"
---
# <span data-ttu-id="bbfd6-101">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="bbfd6-101">Remove-AzureRmRouteTable</span></span>

## <span data-ttu-id="bbfd6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bbfd6-102">SYNOPSIS</span></span>
<span data-ttu-id="bbfd6-103">Usuwa tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="bbfd6-103">Removes a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbfd6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bbfd6-104">SYNTAX</span></span>

```
Remove-AzureRmRouteTable -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbfd6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bbfd6-105">DESCRIPTION</span></span>
<span data-ttu-id="bbfd6-106">Polecenie cmdlet **Remove-AzureRmRouteTable** usuwa tabelę routingu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bbfd6-106">The **Remove-AzureRmRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="bbfd6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bbfd6-107">EXAMPLES</span></span>

### <span data-ttu-id="bbfd6-108">Przykład 1: Usuwanie tabeli tras</span><span class="sxs-lookup"><span data-stu-id="bbfd6-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzureRmRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="bbfd6-109">To polecenie usuwa tabelę routingu o nazwie RouteTable01 w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="bbfd6-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="bbfd6-110">Polecenie cmdlet monituje o potwierdzenie przed usunięciem tabeli.</span><span class="sxs-lookup"><span data-stu-id="bbfd6-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="bbfd6-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bbfd6-111">PARAMETERS</span></span>

### <span data-ttu-id="bbfd6-112">-Force</span><span class="sxs-lookup"><span data-stu-id="bbfd6-112">-Force</span></span>
<span data-ttu-id="bbfd6-113">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="bbfd6-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bbfd6-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bbfd6-114">-Name</span></span>
<span data-ttu-id="bbfd6-115">Określa nazwę tabeli routingu, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbfd6-115">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bbfd6-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bbfd6-116">-PassThru</span></span>
<span data-ttu-id="bbfd6-117">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="bbfd6-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bbfd6-118">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="bbfd6-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bbfd6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbfd6-119">-ResourceGroupName</span></span>
<span data-ttu-id="bbfd6-120">Określa nazwę grupy zasobów zawierającej tabelę tras, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbfd6-120">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bbfd6-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bbfd6-121">-Confirm</span></span>
<span data-ttu-id="bbfd6-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbfd6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbfd6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbfd6-123">-WhatIf</span></span>
<span data-ttu-id="bbfd6-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbfd6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbfd6-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bbfd6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbfd6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbfd6-126">-DefaultProfile</span></span>
<span data-ttu-id="bbfd6-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bbfd6-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbfd6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbfd6-128">CommonParameters</span></span>
<span data-ttu-id="bbfd6-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbfd6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbfd6-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbfd6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbfd6-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bbfd6-131">INPUTS</span></span>

## <span data-ttu-id="bbfd6-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bbfd6-132">OUTPUTS</span></span>

## <span data-ttu-id="bbfd6-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bbfd6-133">NOTES</span></span>

## <span data-ttu-id="bbfd6-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bbfd6-134">RELATED LINKS</span></span>

[<span data-ttu-id="bbfd6-135">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="bbfd6-135">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="bbfd6-136">Nowe — AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="bbfd6-136">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="bbfd6-137">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="bbfd6-137">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


