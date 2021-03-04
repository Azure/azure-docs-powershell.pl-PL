---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 2f100d29b2251d71b170c7833f77ab2f23f90209
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955770"
---
# <span data-ttu-id="cc04b-101">Set-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="cc04b-101">Set-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="cc04b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc04b-102">SYNOPSIS</span></span>
<span data-ttu-id="cc04b-103">Aktualizuje tożsamość przypisaną do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cc04b-103">Updates a identity assigned to the application gateway.</span></span>

## <span data-ttu-id="cc04b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cc04b-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc04b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="cc04b-105">DESCRIPTION</span></span>
<span data-ttu-id="cc04b-106">Polecenie **cmdlet Set-AzApplicationGatewayIdentity** aktualizuje tożsamość przypisaną do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cc04b-106">The **Set-AzApplicationGatewayIdentity** cmdlet updates an identity assigned to application gateway.</span></span>

## <span data-ttu-id="cc04b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cc04b-107">EXAMPLES</span></span>

### <span data-ttu-id="cc04b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cc04b-108">Example 1</span></span>
```powershell
PS C:\>$appgw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$appgwIdentity = Set-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id -ApplicationGateway $appgw
PS C:\>$updatedAppGw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="cc04b-109">W tym przykładzie przypiszemy tożsamość przypisaną do użytkownika do istniejącej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cc04b-109">In this example, we assign a user assigned identity to an existing application gateway.</span></span>
<span data-ttu-id="cc04b-110">Uwaga: Ta tożsamość powinna mieć dostęp do kluczowej informacji, do której będą odwoływowane się certyfikaty/tajemnice.</span><span class="sxs-lookup"><span data-stu-id="cc04b-110">Note: This identity should have access to the keyvault from which the certificates/secrets will be referenced.</span></span>

## <span data-ttu-id="cc04b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc04b-111">PARAMETERS</span></span>

### <span data-ttu-id="cc04b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cc04b-112">-ApplicationGateway</span></span>
<span data-ttu-id="cc04b-113">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="cc04b-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc04b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc04b-114">-DefaultProfile</span></span>
<span data-ttu-id="cc04b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cc04b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc04b-116">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="cc04b-116">-UserAssignedIdentityId</span></span>
<span data-ttu-id="cc04b-117">Identyfikator Zasobu przypisanej tożsamości użytkownika, który ma zostać przypisany do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cc04b-117">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="cc04b-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cc04b-118">-Confirm</span></span>
<span data-ttu-id="cc04b-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cc04b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc04b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc04b-120">-WhatIf</span></span>
<span data-ttu-id="cc04b-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc04b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc04b-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cc04b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc04b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc04b-123">CommonParameters</span></span>
<span data-ttu-id="cc04b-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc04b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc04b-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc04b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc04b-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc04b-126">INPUTS</span></span>

### <span data-ttu-id="cc04b-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cc04b-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="cc04b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="cc04b-128">System.String</span></span>

## <span data-ttu-id="cc04b-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc04b-129">OUTPUTS</span></span>

### <span data-ttu-id="cc04b-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cc04b-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cc04b-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cc04b-131">NOTES</span></span>

## <span data-ttu-id="cc04b-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc04b-132">RELATED LINKS</span></span>
