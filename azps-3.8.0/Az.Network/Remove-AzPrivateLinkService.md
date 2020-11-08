---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
ms.openlocfilehash: 4b95610996aad93144ccaa749c41319cf513ff7f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052971"
---
# <span data-ttu-id="8b1d7-101">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8b1d7-101">Remove-AzPrivateLinkService</span></span>

## <span data-ttu-id="8b1d7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8b1d7-102">SYNOPSIS</span></span>
<span data-ttu-id="8b1d7-103">Usuwa usługę linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="8b1d7-103">Removes a private link service</span></span>

## <span data-ttu-id="8b1d7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8b1d7-104">SYNTAX</span></span>

```
Remove-AzPrivateLinkService -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b1d7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8b1d7-105">DESCRIPTION</span></span>
<span data-ttu-id="8b1d7-106">Polecenie cmdlet **Remove-AzPrivateLinkService** umożliwia usunięcie usługi linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="8b1d7-106">The **Remove-AzPrivateLinkService** cmdlet removes a private link service</span></span>

## <span data-ttu-id="8b1d7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8b1d7-107">EXAMPLES</span></span>

### <span data-ttu-id="8b1d7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8b1d7-108">Example 1</span></span>
```
Remove-AzPrivateLinkService -ResourceGroupName TestResourceGroup -Name TestPrivateLinkService
```

<span data-ttu-id="8b1d7-109">W tym przykładzie usunięto usługę link prywatny o nazwie TestPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="8b1d7-109">This example removes a private link service named TestPrivateLinkService.</span></span>

## <span data-ttu-id="8b1d7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8b1d7-110">PARAMETERS</span></span>

### <span data-ttu-id="8b1d7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b1d7-111">-AsJob</span></span>
<span data-ttu-id="8b1d7-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8b1d7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b1d7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b1d7-113">-DefaultProfile</span></span>
<span data-ttu-id="8b1d7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8b1d7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b1d7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8b1d7-115">-Force</span></span>
<span data-ttu-id="8b1d7-116">Nie pytaj o potwierdzenie, czy chcesz usunąć zasób</span><span class="sxs-lookup"><span data-stu-id="8b1d7-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="8b1d7-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8b1d7-117">-Name</span></span>
<span data-ttu-id="8b1d7-118">Nazwa usługi.</span><span class="sxs-lookup"><span data-stu-id="8b1d7-118">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b1d7-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b1d7-119">-PassThru</span></span>
<span data-ttu-id="8b1d7-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="8b1d7-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8b1d7-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="8b1d7-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8b1d7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b1d7-122">-ResourceGroupName</span></span>
<span data-ttu-id="8b1d7-123">Nazwa grupy zasobów usługi linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="8b1d7-123">The resource group name of the private link service.</span></span>

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

### <span data-ttu-id="8b1d7-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8b1d7-124">-Confirm</span></span>
<span data-ttu-id="8b1d7-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b1d7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b1d7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b1d7-126">-WhatIf</span></span>
<span data-ttu-id="8b1d7-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b1d7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b1d7-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8b1d7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b1d7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b1d7-129">CommonParameters</span></span>
<span data-ttu-id="8b1d7-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b1d7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b1d7-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b1d7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b1d7-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b1d7-132">INPUTS</span></span>

### <span data-ttu-id="8b1d7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8b1d7-133">System.String</span></span>

## <span data-ttu-id="8b1d7-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8b1d7-134">OUTPUTS</span></span>

### <span data-ttu-id="8b1d7-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8b1d7-135">System.Boolean</span></span>

## <span data-ttu-id="8b1d7-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8b1d7-136">NOTES</span></span>

## <span data-ttu-id="8b1d7-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b1d7-137">RELATED LINKS</span></span>

[<span data-ttu-id="8b1d7-138">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8b1d7-138">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="8b1d7-139">Nowe — AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8b1d7-139">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)