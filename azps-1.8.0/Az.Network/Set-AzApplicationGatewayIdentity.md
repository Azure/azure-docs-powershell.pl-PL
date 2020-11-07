---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 83a44e97e01e846cec568227514177babd76d30a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709015"
---
# <span data-ttu-id="25934-101">Set-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="25934-101">Set-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="25934-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="25934-102">SYNOPSIS</span></span>
<span data-ttu-id="25934-103">Aktualizuje tożsamość przypisaną do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="25934-103">Updates a identity assigned to the application gateway.</span></span>

## <span data-ttu-id="25934-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="25934-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25934-105">Opis</span><span class="sxs-lookup"><span data-stu-id="25934-105">DESCRIPTION</span></span>
<span data-ttu-id="25934-106">Polecenie cmdlet **Set-AzApplicationGatewayIdentity** aktualizuje tożsamość przypisaną bramie Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="25934-106">The **Set-AzApplicationGatewayIdentity** cmdlet updates an identity assigned to application gateway.</span></span>

## <span data-ttu-id="25934-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="25934-107">EXAMPLES</span></span>

### <span data-ttu-id="25934-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="25934-108">Example 1</span></span>
```powershell
PS C:\>$appgw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$appgwIdentity = Set-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id -ApplicationGateway $appgw
PS C:\>$updatedAppGw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="25934-109">W tym przykładzie przypiszesz tożsamość przypisanego użytkownikowi do istniejącej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="25934-109">In this example, we assign a user assigned identity to an existing applicaiton gateway.</span></span>
<span data-ttu-id="25934-110">Uwaga: Ta tożsamość powinna mieć dostęp do magazynu kluczy, z którego będą odwoływać się certyfikaty/klucze tajne.</span><span class="sxs-lookup"><span data-stu-id="25934-110">Note: This identity should have access to the keyvault from which the certificates/secrets will be referenced.</span></span>

## <span data-ttu-id="25934-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="25934-111">PARAMETERS</span></span>

### <span data-ttu-id="25934-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="25934-112">-ApplicationGateway</span></span>
<span data-ttu-id="25934-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="25934-113">The applicationGateway</span></span>

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

### <span data-ttu-id="25934-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25934-114">-DefaultProfile</span></span>
<span data-ttu-id="25934-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="25934-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25934-116">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="25934-116">-UserAssignedIdentityId</span></span>
<span data-ttu-id="25934-117">Identyfikator ResourceId przypisanego użytkownikowi tożsamości, który ma zostać przypisany do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="25934-117">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="25934-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="25934-118">-Confirm</span></span>
<span data-ttu-id="25934-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25934-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25934-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25934-120">-WhatIf</span></span>
<span data-ttu-id="25934-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25934-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25934-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="25934-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25934-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25934-123">CommonParameters</span></span>
<span data-ttu-id="25934-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25934-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25934-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25934-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25934-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25934-126">INPUTS</span></span>

### <span data-ttu-id="25934-127">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="25934-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="25934-128">System. String</span><span class="sxs-lookup"><span data-stu-id="25934-128">System.String</span></span>

## <span data-ttu-id="25934-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="25934-129">OUTPUTS</span></span>

### <span data-ttu-id="25934-130">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="25934-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="25934-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="25934-131">NOTES</span></span>

## <span data-ttu-id="25934-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25934-132">RELATED LINKS</span></span>
