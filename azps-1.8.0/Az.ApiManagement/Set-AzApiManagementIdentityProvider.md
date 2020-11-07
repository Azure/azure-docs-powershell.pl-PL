---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
ms.openlocfilehash: f8bc49e4a5b4e8e7fb6285327cf4432cd0561506
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869340"
---
# <span data-ttu-id="6d1bc-101">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="6d1bc-101">Set-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="6d1bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6d1bc-102">SYNOPSIS</span></span>
<span data-ttu-id="6d1bc-103">Umożliwia zaktualizowanie konfiguracji istniejącego dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="6d1bc-103">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="6d1bc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6d1bc-104">SYNTAX</span></span>

```
Set-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d1bc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6d1bc-105">DESCRIPTION</span></span>
<span data-ttu-id="6d1bc-106">Umożliwia zaktualizowanie konfiguracji istniejącego dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="6d1bc-106">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="6d1bc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6d1bc-107">EXAMPLES</span></span>

### <span data-ttu-id="6d1bc-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6d1bc-108">Example 1</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Set-AzApiManagementIdentityProvider -Context $apimContext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="6d1bc-109">Polecenie cmdlet aktualizuje klucz tajny klienta usługi Facebook Identity Provider.</span><span class="sxs-lookup"><span data-stu-id="6d1bc-109">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="6d1bc-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6d1bc-110">PARAMETERS</span></span>

### <span data-ttu-id="6d1bc-111">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="6d1bc-111">-AllowedTenants</span></span>
<span data-ttu-id="6d1bc-112">Lista dozwolonych dzierżaw usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6d1bc-112">List of allowed Azure Active Directory Tenants.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d1bc-113">-ClientId</span><span class="sxs-lookup"><span data-stu-id="6d1bc-113">-ClientId</span></span>
<span data-ttu-id="6d1bc-114">Identyfikator klienta aplikacji w zewnętrznym dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="6d1bc-114">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="6d1bc-115">Jest to identyfikator aplikacji dla logowania do serwisu Facebook, identyfikator klienta Google login, identyfikator aplikacji dla firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6d1bc-115">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d1bc-116">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="6d1bc-116">-ClientSecret</span></span>
<span data-ttu-id="6d1bc-117">Klucz tajny klienta aplikacji w zewnętrznym dostawcy tożsamości, służący do uwierzytelniania żądania logowania.</span><span class="sxs-lookup"><span data-stu-id="6d1bc-117">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="6d1bc-118">Na przykład jest to klucz tajny aplikacji dla logowania do serwisu Facebook, klucz interfejsu API logowania Google, klucz publiczny dla firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6d1bc-118">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d1bc-119">-Context</span><span class="sxs-lookup"><span data-stu-id="6d1bc-119">-Context</span></span>
<span data-ttu-id="6d1bc-120">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6d1bc-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6d1bc-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="6d1bc-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d1bc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d1bc-122">-DefaultProfile</span></span>
<span data-ttu-id="6d1bc-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6d1bc-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d1bc-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d1bc-124">-PassThru</span></span>
<span data-ttu-id="6d1bc-125">Wskazuje, że to polecenie cmdlet zwróci  **PsApiManagementIdentityProvider** , które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d1bc-125">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="6d1bc-126">-Type</span><span class="sxs-lookup"><span data-stu-id="6d1bc-126">-Type</span></span>
<span data-ttu-id="6d1bc-127">Identyfikator istniejącego dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="6d1bc-127">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="6d1bc-128">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="6d1bc-128">This parameter is required.</span></span>

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

### <span data-ttu-id="6d1bc-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6d1bc-129">-Confirm</span></span>
<span data-ttu-id="6d1bc-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d1bc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d1bc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d1bc-131">-WhatIf</span></span>
<span data-ttu-id="6d1bc-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d1bc-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d1bc-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6d1bc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d1bc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d1bc-134">CommonParameters</span></span>
<span data-ttu-id="6d1bc-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d1bc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d1bc-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d1bc-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d1bc-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d1bc-137">INPUTS</span></span>

### <span data-ttu-id="6d1bc-138">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6d1bc-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6d1bc-139">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="6d1bc-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="6d1bc-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6d1bc-140">System.String</span></span>

### <span data-ttu-id="6d1bc-141">System. String []</span><span class="sxs-lookup"><span data-stu-id="6d1bc-141">System.String[]</span></span>

### <span data-ttu-id="6d1bc-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6d1bc-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6d1bc-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6d1bc-143">OUTPUTS</span></span>

### <span data-ttu-id="6d1bc-144">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="6d1bc-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="6d1bc-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6d1bc-145">NOTES</span></span>

## <span data-ttu-id="6d1bc-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d1bc-146">RELATED LINKS</span></span>

[<span data-ttu-id="6d1bc-147">Nowe — AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="6d1bc-147">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="6d1bc-148">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="6d1bc-148">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="6d1bc-149">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="6d1bc-149">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)
