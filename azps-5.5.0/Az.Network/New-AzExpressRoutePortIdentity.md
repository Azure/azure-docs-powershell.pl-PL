---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
ms.openlocfilehash: d19acf8bb97f3b84b3cd831e4cf91397231f4b08
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189690"
---
# <span data-ttu-id="f218e-101">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="f218e-101">New-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="f218e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f218e-102">SYNOPSIS</span></span>
<span data-ttu-id="f218e-103">Tworzy usługę Azure ExpressRoutePortIdentity.</span><span class="sxs-lookup"><span data-stu-id="f218e-103">Creates an Azure ExpressRoutePortIdentity.</span></span>

## <span data-ttu-id="f218e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f218e-104">SYNTAX</span></span>

```
New-AzExpressRoutePortIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f218e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f218e-105">DESCRIPTION</span></span>
<span data-ttu-id="f218e-106">Polecenie **cmdlet New-AzExpressRoutePortIdentity** tworzy lokalny obiekt tożsamości usługi Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="f218e-106">The **New-AzExpressRoutePortIdentity** cmdlet creates a local Azure ExpressRoutePort Identity object.</span></span> <span data-ttu-id="f218e-107">Użyj **wyrażenia New-azExpressRoutePort** lub **Set-AzExpressRoutePort,** aby przypisać je do usługi Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="f218e-107">Use **New-AzExpressRoutePort** or **Set-AzExpressRoutePort** to assign it to Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="f218e-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f218e-108">EXAMPLES</span></span>

### <span data-ttu-id="f218e-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f218e-109">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    UserAssignedIdentityId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<IdentityName>'
    }
PS C:\> New-AzExpressRoutePortIdentity @parameters
```

## <span data-ttu-id="f218e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f218e-110">PARAMETERS</span></span>

### <span data-ttu-id="f218e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f218e-111">-DefaultProfile</span></span>
<span data-ttu-id="f218e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f218e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f218e-113">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="f218e-113">-UserAssignedIdentityId</span></span>
<span data-ttu-id="f218e-114">Identyfikator Zasobu przypisanej tożsamości użytkownika, który ma zostać przypisany do portu ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="f218e-114">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="f218e-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f218e-115">-Confirm</span></span>
<span data-ttu-id="f218e-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f218e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f218e-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f218e-117">-WhatIf</span></span>
<span data-ttu-id="f218e-118">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f218e-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f218e-119">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f218e-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f218e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f218e-120">CommonParameters</span></span>
<span data-ttu-id="f218e-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f218e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f218e-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f218e-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f218e-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f218e-123">INPUTS</span></span>

### <span data-ttu-id="f218e-124">System.String</span><span class="sxs-lookup"><span data-stu-id="f218e-124">System.String</span></span>

## <span data-ttu-id="f218e-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f218e-125">OUTPUTS</span></span>

### <span data-ttu-id="f218e-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="f218e-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="f218e-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f218e-127">NOTES</span></span>

## <span data-ttu-id="f218e-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f218e-128">RELATED LINKS</span></span>
[<span data-ttu-id="f218e-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="f218e-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="f218e-130">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="f218e-130">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="f218e-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="f218e-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)