---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 76ee402fee2e18d426875340d4eaadda2cc63042
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548439"
---
# <span data-ttu-id="dea10-101">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="dea10-101">Set-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="dea10-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dea10-102">SYNOPSIS</span></span>
<span data-ttu-id="dea10-103">Umożliwia zaktualizowanie konfiguracji istniejącego dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="dea10-103">Updates the Configuration of an existing Identity Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dea10-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dea10-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dea10-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dea10-105">DESCRIPTION</span></span>
<span data-ttu-id="dea10-106">Umożliwia zaktualizowanie konfiguracji istniejącego dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="dea10-106">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="dea10-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dea10-107">EXAMPLES</span></span>

### <span data-ttu-id="dea10-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dea10-108">Example 1</span></span>
```
PS C:\> Set-AzureRmApiManagementIdentityProvider -Context $apimcontext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="dea10-109">Polecenie cmdlet aktualizuje klucz tajny klienta usługi Facebook Identity Provider.</span><span class="sxs-lookup"><span data-stu-id="dea10-109">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="dea10-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dea10-110">PARAMETERS</span></span>

### <span data-ttu-id="dea10-111">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="dea10-111">-AllowedTenants</span></span>
<span data-ttu-id="dea10-112">Lista dozwolonych dzierżaw usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dea10-112">List of allowed Azure Active Directory Tenants.</span></span>

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

### <span data-ttu-id="dea10-113">-ClientId</span><span class="sxs-lookup"><span data-stu-id="dea10-113">-ClientId</span></span>
<span data-ttu-id="dea10-114">Identyfikator klienta aplikacji w zewnętrznym dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="dea10-114">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="dea10-115">Jest to identyfikator aplikacji dla logowania do serwisu Facebook, identyfikator klienta Google login, identyfikator aplikacji dla firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dea10-115">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="dea10-116">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="dea10-116">-ClientSecret</span></span>
<span data-ttu-id="dea10-117">Klucz tajny klienta aplikacji w zewnętrznym dostawcy tożsamości, służący do uwierzytelniania żądania logowania.</span><span class="sxs-lookup"><span data-stu-id="dea10-117">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="dea10-118">Na przykład jest to klucz tajny aplikacji dla logowania do serwisu Facebook, klucz interfejsu API logowania Google, klucz publiczny dla firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dea10-118">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="dea10-119">-Context</span><span class="sxs-lookup"><span data-stu-id="dea10-119">-Context</span></span>
<span data-ttu-id="dea10-120">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="dea10-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="dea10-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="dea10-121">This parameter is required.</span></span>

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

### <span data-ttu-id="dea10-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dea10-122">-PassThru</span></span>
<span data-ttu-id="dea10-123">Wskazuje, że to polecenie cmdlet zwróci  **PsApiManagementIdentityProvider** , które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dea10-123">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>


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

### <span data-ttu-id="dea10-124">-Type</span><span class="sxs-lookup"><span data-stu-id="dea10-124">-Type</span></span>
<span data-ttu-id="dea10-125">Identyfikator istniejącego dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="dea10-125">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="dea10-126">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="dea10-126">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dea10-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dea10-127">-Confirm</span></span>
<span data-ttu-id="dea10-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dea10-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dea10-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dea10-129">-WhatIf</span></span>
<span data-ttu-id="dea10-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dea10-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dea10-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dea10-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dea10-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dea10-132">-DefaultProfile</span></span>
<span data-ttu-id="dea10-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dea10-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dea10-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dea10-134">CommonParameters</span></span>
<span data-ttu-id="dea10-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dea10-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dea10-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dea10-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dea10-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dea10-137">INPUTS</span></span>

## <span data-ttu-id="dea10-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dea10-138">OUTPUTS</span></span>

### <span data-ttu-id="dea10-139">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="dea10-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="dea10-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dea10-140">NOTES</span></span>

## <span data-ttu-id="dea10-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dea10-141">RELATED LINKS</span></span>

[<span data-ttu-id="dea10-142">Nowe — AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="dea10-142">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="dea10-143">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="dea10-143">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="dea10-144">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="dea10-144">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)
