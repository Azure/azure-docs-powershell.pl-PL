---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
ms.openlocfilehash: e32c0912026555f9b85a83720d1c7c48a5170f70
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202915"
---
# <span data-ttu-id="58390-101">New-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="58390-101">New-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="58390-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58390-102">SYNOPSIS</span></span>
<span data-ttu-id="58390-103">Tworzy obiekt tożsamości dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="58390-103">Creates an identity object for an application gateway.</span></span> <span data-ttu-id="58390-104">Spowoduje to przypisanie odwołania do tożsamości przypisanej przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="58390-104">This will hold reference to the user assigned identity.</span></span>

## <span data-ttu-id="58390-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="58390-105">SYNTAX</span></span>

```
New-AzApplicationGatewayIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58390-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="58390-106">DESCRIPTION</span></span>
<span data-ttu-id="58390-107">**Polecenie cmdlet New-AzApplicationGatewayIdentity** tworzy obiekt tożsamości bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="58390-107">**New-AzApplicationGatewayIdentity** cmdlet creates an application gateway identity object.</span></span>

## <span data-ttu-id="58390-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="58390-108">EXAMPLES</span></span>

### <span data-ttu-id="58390-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="58390-109">Example 1</span></span>
```powershell
PS C:\> $identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\> $appgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id
PS C:\> $gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $appgwIdentity <..>
```

<span data-ttu-id="58390-110">W tym przykładzie tworzymy tożsamość przypisaną do użytkownika, a następnie odwołujemy się do niego w obiekcie tożsamości używanym z bramą aplikacji.</span><span class="sxs-lookup"><span data-stu-id="58390-110">In this example, we create a user assigned identity and then reference it in identity object used with Application Gateway.</span></span>

## <span data-ttu-id="58390-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58390-111">PARAMETERS</span></span>

### <span data-ttu-id="58390-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58390-112">-DefaultProfile</span></span>
<span data-ttu-id="58390-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="58390-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58390-114">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="58390-114">-UserAssignedIdentityId</span></span>
<span data-ttu-id="58390-115">Identyfikator Zasobu przypisanej tożsamości użytkownika, który ma zostać przypisany do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="58390-115">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="58390-116">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="58390-116">-Confirm</span></span>
<span data-ttu-id="58390-117">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="58390-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58390-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58390-118">-WhatIf</span></span>
<span data-ttu-id="58390-119">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58390-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58390-120">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="58390-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58390-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58390-121">CommonParameters</span></span>
<span data-ttu-id="58390-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58390-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58390-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58390-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58390-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58390-124">INPUTS</span></span>

### <span data-ttu-id="58390-125">System.String</span><span class="sxs-lookup"><span data-stu-id="58390-125">System.String</span></span>

## <span data-ttu-id="58390-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="58390-126">OUTPUTS</span></span>

### <span data-ttu-id="58390-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="58390-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="58390-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="58390-128">NOTES</span></span>

## <span data-ttu-id="58390-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58390-129">RELATED LINKS</span></span>
