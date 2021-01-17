---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
ms.openlocfilehash: e15e6757d6a4d0f6e84a9580877deecdeede94ee
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382048"
---
# <span data-ttu-id="4cfe2-101">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4cfe2-101">Remove-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="4cfe2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4cfe2-102">SYNOPSIS</span></span>
<span data-ttu-id="4cfe2-103">Usuwa istniejącą konfigurację dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="4cfe2-103">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="4cfe2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4cfe2-104">SYNTAX</span></span>

```
Remove-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cfe2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4cfe2-105">DESCRIPTION</span></span>
<span data-ttu-id="4cfe2-106">Usuwa istniejącą konfigurację dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="4cfe2-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="4cfe2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4cfe2-107">EXAMPLES</span></span>

### <span data-ttu-id="4cfe2-108">Przykład 1: usuwa ustawienia dostawcy tożsamości w serwisie Facebook z usługi ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4cfe2-108">Example 1: Removes the Facebook identity provider settings from ApiManagement service</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="4cfe2-109">Usuwa konfigurację dotyczącą konfiguracji dostawcy tożsamości w serwisie Facebook.</span><span class="sxs-lookup"><span data-stu-id="4cfe2-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="4cfe2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4cfe2-110">PARAMETERS</span></span>

### <span data-ttu-id="4cfe2-111">-Context</span><span class="sxs-lookup"><span data-stu-id="4cfe2-111">-Context</span></span>
<span data-ttu-id="4cfe2-112">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="4cfe2-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4cfe2-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="4cfe2-113">This parameter is required.</span></span>

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

### <span data-ttu-id="4cfe2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cfe2-114">-DefaultProfile</span></span>
<span data-ttu-id="4cfe2-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4cfe2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cfe2-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4cfe2-116">-PassThru</span></span>
<span data-ttu-id="4cfe2-117">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli operacja się powiedzie lub $False w inny sposób.</span><span class="sxs-lookup"><span data-stu-id="4cfe2-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="4cfe2-118">-Type</span><span class="sxs-lookup"><span data-stu-id="4cfe2-118">-Type</span></span>
<span data-ttu-id="4cfe2-119">Identyfikator istniejącego dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="4cfe2-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="4cfe2-120">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="4cfe2-120">This parameter is required.</span></span>

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

### <span data-ttu-id="4cfe2-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4cfe2-121">-Confirm</span></span>
<span data-ttu-id="4cfe2-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cfe2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cfe2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cfe2-123">-WhatIf</span></span>
<span data-ttu-id="4cfe2-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cfe2-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4cfe2-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4cfe2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cfe2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cfe2-126">CommonParameters</span></span>
<span data-ttu-id="4cfe2-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cfe2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cfe2-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4cfe2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cfe2-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cfe2-129">INPUTS</span></span>

### <span data-ttu-id="4cfe2-130">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4cfe2-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4cfe2-131">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="4cfe2-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="4cfe2-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4cfe2-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4cfe2-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4cfe2-133">OUTPUTS</span></span>

### <span data-ttu-id="4cfe2-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4cfe2-134">System.Boolean</span></span>

## <span data-ttu-id="4cfe2-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4cfe2-135">NOTES</span></span>

## <span data-ttu-id="4cfe2-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4cfe2-136">RELATED LINKS</span></span>

[<span data-ttu-id="4cfe2-137">Nowe — AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4cfe2-137">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="4cfe2-138">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4cfe2-138">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="4cfe2-139">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4cfe2-139">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)

