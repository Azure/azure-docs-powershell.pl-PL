---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
ms.openlocfilehash: d19acf8bb97f3b84b3cd831e4cf91397231f4b08
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050627"
---
# <span data-ttu-id="aa327-101">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="aa327-101">New-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="aa327-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa327-102">SYNOPSIS</span></span>
<span data-ttu-id="aa327-103">Tworzy usługę Azure ExpressRoutePortIdentity.</span><span class="sxs-lookup"><span data-stu-id="aa327-103">Creates an Azure ExpressRoutePortIdentity.</span></span>

## <span data-ttu-id="aa327-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa327-104">SYNTAX</span></span>

```
New-AzExpressRoutePortIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa327-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aa327-105">DESCRIPTION</span></span>
<span data-ttu-id="aa327-106">Polecenie cmdlet **New-AzExpressRoutePortIdentity** tworzy obiekt Local Azure ExpressRoutePort Identity.</span><span class="sxs-lookup"><span data-stu-id="aa327-106">The **New-AzExpressRoutePortIdentity** cmdlet creates a local Azure ExpressRoutePort Identity object.</span></span> <span data-ttu-id="aa327-107">Aby przypisać ją do usługi Azure ExpressRoutePort, użyj **nowych-AzExpressRoutePort** lub **Set-AzExpressRoutePort** .</span><span class="sxs-lookup"><span data-stu-id="aa327-107">Use **New-AzExpressRoutePort** or **Set-AzExpressRoutePort** to assign it to Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="aa327-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa327-108">EXAMPLES</span></span>

### <span data-ttu-id="aa327-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="aa327-109">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    UserAssignedIdentityId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<IdentityName>'
    }
PS C:\> New-AzExpressRoutePortIdentity @parameters
```

## <span data-ttu-id="aa327-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa327-110">PARAMETERS</span></span>

### <span data-ttu-id="aa327-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa327-111">-DefaultProfile</span></span>
<span data-ttu-id="aa327-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa327-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa327-113">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="aa327-113">-UserAssignedIdentityId</span></span>
<span data-ttu-id="aa327-114">Identyfikator ResourceId przypisanego użytkownikowi tożsamości, który ma zostać przypisany do ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="aa327-114">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="aa327-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aa327-115">-Confirm</span></span>
<span data-ttu-id="aa327-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa327-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa327-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa327-117">-WhatIf</span></span>
<span data-ttu-id="aa327-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa327-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa327-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="aa327-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa327-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa327-120">CommonParameters</span></span>
<span data-ttu-id="aa327-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa327-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa327-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa327-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa327-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa327-123">INPUTS</span></span>

### <span data-ttu-id="aa327-124">System. String</span><span class="sxs-lookup"><span data-stu-id="aa327-124">System.String</span></span>

## <span data-ttu-id="aa327-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa327-125">OUTPUTS</span></span>

### <span data-ttu-id="aa327-126">Microsoft. Azure. Commands. Network. models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="aa327-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="aa327-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa327-127">NOTES</span></span>

## <span data-ttu-id="aa327-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa327-128">RELATED LINKS</span></span>
[<span data-ttu-id="aa327-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="aa327-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="aa327-130">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="aa327-130">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="aa327-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="aa327-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)