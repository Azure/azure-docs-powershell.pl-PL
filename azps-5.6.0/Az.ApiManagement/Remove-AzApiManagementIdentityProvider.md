---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
ms.openlocfilehash: f80fe2b09be6d4bdc624f65de014d3b7f1beadd6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015530"
---
# <span data-ttu-id="ec996-101">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="ec996-101">Remove-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="ec996-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec996-102">SYNOPSIS</span></span>
<span data-ttu-id="ec996-103">Usuwa istniejącą konfigurację dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="ec996-103">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="ec996-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ec996-104">SYNTAX</span></span>

```
Remove-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec996-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ec996-105">DESCRIPTION</span></span>
<span data-ttu-id="ec996-106">Usuwa istniejącą konfigurację dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="ec996-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="ec996-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ec996-107">EXAMPLES</span></span>

### <span data-ttu-id="ec996-108">Przykład 1. Usunięcie ustawień dostawcy tożsamości serwisu Facebook z usługi ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ec996-108">Example 1: Removes the Facebook identity provider settings from ApiManagement service</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="ec996-109">Usuwa konfigurację związaną z konfiguracją dostawcy tożsamości serwisu Facebook.</span><span class="sxs-lookup"><span data-stu-id="ec996-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="ec996-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec996-110">PARAMETERS</span></span>

### <span data-ttu-id="ec996-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="ec996-111">-Context</span></span>
<span data-ttu-id="ec996-112">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ec996-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ec996-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="ec996-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec996-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec996-114">-DefaultProfile</span></span>
<span data-ttu-id="ec996-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ec996-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec996-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec996-116">-PassThru</span></span>
<span data-ttu-id="ec996-117">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli operacja się powiedzie lub $False w inny sposób.</span><span class="sxs-lookup"><span data-stu-id="ec996-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec996-118">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="ec996-118">-Type</span></span>
<span data-ttu-id="ec996-119">Identyfikator istniejącego dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="ec996-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="ec996-120">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="ec996-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec996-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ec996-121">-Confirm</span></span>
<span data-ttu-id="ec996-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ec996-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec996-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec996-123">-WhatIf</span></span>
<span data-ttu-id="ec996-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec996-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec996-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ec996-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec996-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec996-126">CommonParameters</span></span>
<span data-ttu-id="ec996-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec996-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec996-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec996-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec996-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec996-129">INPUTS</span></span>

### <span data-ttu-id="ec996-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ec996-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ec996-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="ec996-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="ec996-132">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="ec996-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ec996-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec996-133">OUTPUTS</span></span>

### <span data-ttu-id="ec996-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ec996-134">System.Boolean</span></span>

## <span data-ttu-id="ec996-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ec996-135">NOTES</span></span>

## <span data-ttu-id="ec996-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec996-136">RELATED LINKS</span></span>

[<span data-ttu-id="ec996-137">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="ec996-137">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="ec996-138">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="ec996-138">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="ec996-139">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="ec996-139">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)

