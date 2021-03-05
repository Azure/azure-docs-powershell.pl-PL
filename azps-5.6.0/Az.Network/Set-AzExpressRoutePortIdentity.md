---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
ms.openlocfilehash: 6292c2fd19ff61e347291d3aba7e9840799e3b93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976561"
---
# <span data-ttu-id="be18c-101">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="be18c-101">Set-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="be18c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be18c-102">SYNOPSIS</span></span>
<span data-ttu-id="be18c-103">Aktualizuje tożsamość przypisaną do portu ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="be18c-103">Updates a identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="be18c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="be18c-104">SYNTAX</span></span>

```
Set-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be18c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="be18c-105">DESCRIPTION</span></span>
<span data-ttu-id="be18c-106">Polecenie **cmdlet Set-AzExpressRoutePortIdentity** aktualizuje lokalny obiekt Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="be18c-106">The **Set-AzExpressRoutePortIdentity** cmdlet updates a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="be18c-107">Użyj **wyrażenia Set-AzExpressRoutePort,** aby przypisać je do wyrażenia ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="be18c-107">Use **Set-AzExpressRoutePort** to assign it to ExpressRoutePort.</span></span>

## <span data-ttu-id="be18c-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="be18c-108">EXAMPLES</span></span>

### <span data-ttu-id="be18c-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="be18c-109">Example 1</span></span>
```powershell
PS C:\>$exrport = Get-AzExpressRoutePort -Name $portName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$exrPortIdentity = Set-AzExpressRoutePortIdentity -UserAssignedIdentity $identity.Id -ExpressRoutePort $exrPort
PS C:\>$updatedExrPort = Set-AzExpressRoutePort -ExpressRoutePort $exrPort
```

## <span data-ttu-id="be18c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be18c-110">PARAMETERS</span></span>

### <span data-ttu-id="be18c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be18c-111">-DefaultProfile</span></span>
<span data-ttu-id="be18c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="be18c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be18c-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="be18c-113">-ExpressRoutePort</span></span>
<span data-ttu-id="be18c-114">The ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="be18c-114">The ExpressRoutePort</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be18c-115">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="be18c-115">-UserAssignedIdentityId</span></span>
<span data-ttu-id="be18c-116">Identyfikator Zasobu przypisanej tożsamości użytkownika, który ma zostać przypisany do portu ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="be18c-116">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: UserAssignedIdentity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be18c-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="be18c-117">-Confirm</span></span>
<span data-ttu-id="be18c-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="be18c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be18c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be18c-119">-WhatIf</span></span>
<span data-ttu-id="be18c-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be18c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be18c-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="be18c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be18c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be18c-122">CommonParameters</span></span>
<span data-ttu-id="be18c-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be18c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be18c-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be18c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be18c-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be18c-125">INPUTS</span></span>

### <span data-ttu-id="be18c-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="be18c-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="be18c-127">System.String</span><span class="sxs-lookup"><span data-stu-id="be18c-127">System.String</span></span>

## <span data-ttu-id="be18c-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be18c-128">OUTPUTS</span></span>

### <span data-ttu-id="be18c-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="be18c-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="be18c-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="be18c-130">NOTES</span></span>

## <span data-ttu-id="be18c-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be18c-131">RELATED LINKS</span></span>
[<span data-ttu-id="be18c-132">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="be18c-132">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="be18c-133">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="be18c-133">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="be18c-134">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="be18c-134">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)
