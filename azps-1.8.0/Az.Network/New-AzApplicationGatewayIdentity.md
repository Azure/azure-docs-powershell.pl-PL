---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 3bb2df6349c734e9802183c13eb39ae8ceafc50b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709369"
---
# <span data-ttu-id="7f8bc-101">New-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="7f8bc-101">New-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="7f8bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7f8bc-102">SYNOPSIS</span></span>
<span data-ttu-id="7f8bc-103">Tworzy obiekt Identity dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7f8bc-103">Creates an identity object for an application gateway.</span></span> <span data-ttu-id="7f8bc-104">Spowoduje to zablokowanie odwołania do tożsamości przypisanej do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7f8bc-104">This will hold reference to the user assigned identity.</span></span>

## <span data-ttu-id="7f8bc-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7f8bc-105">SYNTAX</span></span>

```
New-AzApplicationGatewayIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f8bc-106">Opis</span><span class="sxs-lookup"><span data-stu-id="7f8bc-106">DESCRIPTION</span></span>
<span data-ttu-id="7f8bc-107">Polecenie cmdlet **New-AzApplicationGatewayIdentity** tworzy obiekt tożsamości bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7f8bc-107">**New-AzApplicationGatewayIdentity** cmdlet creates an application gateway identity object.</span></span>

## <span data-ttu-id="7f8bc-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7f8bc-108">EXAMPLES</span></span>

### <span data-ttu-id="7f8bc-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7f8bc-109">Example 1</span></span>
```powershell
PS C:\> $identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\> $appgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id
PS C:\> $gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $appgwIdentity <..>
```

<span data-ttu-id="7f8bc-110">W tym przykładzie tworzymy tożsamość przydzieloną użytkownikowi, a następnie odwołujesz się do niej w obiekcie Identity (tożsamość), który jest wykorzystywany z bramą Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7f8bc-110">In this example, we create a user assigned identity and then reference it in identity object used with Application Gateway.</span></span>

## <span data-ttu-id="7f8bc-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7f8bc-111">PARAMETERS</span></span>

### <span data-ttu-id="7f8bc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f8bc-112">-DefaultProfile</span></span>
<span data-ttu-id="7f8bc-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7f8bc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f8bc-114">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="7f8bc-114">-UserAssignedIdentityId</span></span>
<span data-ttu-id="7f8bc-115">Identyfikator ResourceId przypisanego użytkownikowi tożsamości, który ma zostać przypisany do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7f8bc-115">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="7f8bc-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7f8bc-116">-Confirm</span></span>
<span data-ttu-id="7f8bc-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f8bc-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f8bc-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f8bc-118">-WhatIf</span></span>
<span data-ttu-id="7f8bc-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f8bc-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f8bc-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7f8bc-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f8bc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f8bc-121">CommonParameters</span></span>
<span data-ttu-id="7f8bc-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f8bc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f8bc-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f8bc-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f8bc-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f8bc-124">INPUTS</span></span>

### <span data-ttu-id="7f8bc-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7f8bc-125">System.String</span></span>

## <span data-ttu-id="7f8bc-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7f8bc-126">OUTPUTS</span></span>

### <span data-ttu-id="7f8bc-127">Microsoft. Azure. Commands. Network. models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="7f8bc-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="7f8bc-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7f8bc-128">NOTES</span></span>

## <span data-ttu-id="7f8bc-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f8bc-129">RELATED LINKS</span></span>
