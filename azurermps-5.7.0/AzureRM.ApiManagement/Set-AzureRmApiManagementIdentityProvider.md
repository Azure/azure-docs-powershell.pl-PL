---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: e45ec5a3d49bf82ab945a3ef3b41362a1e1e2bd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553702"
---
# <span data-ttu-id="49450-101">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="49450-101">Set-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="49450-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="49450-102">SYNOPSIS</span></span>
<span data-ttu-id="49450-103">Umożliwia zaktualizowanie konfiguracji istniejącego dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="49450-103">Updates the Configuration of an existing Identity Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49450-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="49450-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49450-105">Opis</span><span class="sxs-lookup"><span data-stu-id="49450-105">DESCRIPTION</span></span>
<span data-ttu-id="49450-106">Umożliwia zaktualizowanie konfiguracji istniejącego dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="49450-106">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="49450-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="49450-107">EXAMPLES</span></span>

### <span data-ttu-id="49450-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="49450-108">Example 1</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Set-AzureRmApiManagementIdentityProvider -Context $apimContext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="49450-109">Polecenie cmdlet aktualizuje klucz tajny klienta usługi Facebook Identity Provider.</span><span class="sxs-lookup"><span data-stu-id="49450-109">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="49450-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="49450-110">PARAMETERS</span></span>

### <span data-ttu-id="49450-111">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="49450-111">-AllowedTenants</span></span>
<span data-ttu-id="49450-112">Lista dozwolonych dzierżaw usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="49450-112">List of allowed Azure Active Directory Tenants.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49450-113">-ClientId</span><span class="sxs-lookup"><span data-stu-id="49450-113">-ClientId</span></span>
<span data-ttu-id="49450-114">Identyfikator klienta aplikacji w zewnętrznym dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="49450-114">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="49450-115">Jest to identyfikator aplikacji dla logowania do serwisu Facebook, identyfikator klienta Google login, identyfikator aplikacji dla firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="49450-115">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49450-116">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="49450-116">-ClientSecret</span></span>
<span data-ttu-id="49450-117">Klucz tajny klienta aplikacji w zewnętrznym dostawcy tożsamości, służący do uwierzytelniania żądania logowania.</span><span class="sxs-lookup"><span data-stu-id="49450-117">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="49450-118">Na przykład jest to klucz tajny aplikacji dla logowania do serwisu Facebook, klucz interfejsu API logowania Google, klucz publiczny dla firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="49450-118">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49450-119">-Context</span><span class="sxs-lookup"><span data-stu-id="49450-119">-Context</span></span>
<span data-ttu-id="49450-120">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="49450-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="49450-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="49450-121">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49450-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49450-122">-DefaultProfile</span></span>
<span data-ttu-id="49450-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="49450-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49450-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49450-124">-PassThru</span></span>
<span data-ttu-id="49450-125">Wskazuje, że to polecenie cmdlet zwróci  **PsApiManagementIdentityProvider** , które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49450-125">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49450-126">-Type</span><span class="sxs-lookup"><span data-stu-id="49450-126">-Type</span></span>
<span data-ttu-id="49450-127">Identyfikator istniejącego dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="49450-127">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="49450-128">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="49450-128">This parameter is required.</span></span>

```yaml
Type: PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49450-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="49450-129">-Confirm</span></span>
<span data-ttu-id="49450-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49450-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49450-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49450-131">-WhatIf</span></span>
<span data-ttu-id="49450-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49450-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49450-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="49450-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49450-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49450-134">CommonParameters</span></span>
<span data-ttu-id="49450-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49450-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49450-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49450-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49450-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49450-137">INPUTS</span></span>

### <span data-ttu-id="49450-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="49450-138">None</span></span>
<span data-ttu-id="49450-139">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="49450-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="49450-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="49450-140">OUTPUTS</span></span>

### <span data-ttu-id="49450-141">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="49450-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="49450-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="49450-142">NOTES</span></span>

## <span data-ttu-id="49450-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49450-143">RELATED LINKS</span></span>

[<span data-ttu-id="49450-144">Nowe — AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="49450-144">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="49450-145">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="49450-145">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="49450-146">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="49450-146">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)
