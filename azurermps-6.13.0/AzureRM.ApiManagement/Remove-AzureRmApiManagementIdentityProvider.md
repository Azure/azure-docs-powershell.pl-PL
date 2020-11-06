---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: d8cc54570b1282889a93c803e1216096cde35b27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524686"
---
# <span data-ttu-id="d3361-101">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="d3361-101">Remove-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="d3361-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d3361-102">SYNOPSIS</span></span>
<span data-ttu-id="d3361-103">Usuwa istniejącą konfigurację dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="d3361-103">Removes an existing Identity Provider Configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3361-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d3361-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3361-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d3361-105">DESCRIPTION</span></span>
<span data-ttu-id="d3361-106">Usuwa istniejącą konfigurację dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="d3361-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="d3361-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d3361-107">EXAMPLES</span></span>

### <span data-ttu-id="d3361-108">Usuwa ustawienia dostawcy tożsamości w serwisie Facebook z usługi ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d3361-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="d3361-109">Usuwa konfigurację dotyczącą konfiguracji dostawcy tożsamości w serwisie Facebook.</span><span class="sxs-lookup"><span data-stu-id="d3361-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="d3361-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d3361-110">PARAMETERS</span></span>

### <span data-ttu-id="d3361-111">-Context</span><span class="sxs-lookup"><span data-stu-id="d3361-111">-Context</span></span>
<span data-ttu-id="d3361-112">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d3361-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d3361-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="d3361-113">This parameter is required.</span></span>

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

### <span data-ttu-id="d3361-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3361-114">-DefaultProfile</span></span>
<span data-ttu-id="d3361-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d3361-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3361-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3361-116">-PassThru</span></span>
<span data-ttu-id="d3361-117">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli operacja się powiedzie lub $False w inny sposób.</span><span class="sxs-lookup"><span data-stu-id="d3361-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="d3361-118">-Type</span><span class="sxs-lookup"><span data-stu-id="d3361-118">-Type</span></span>
<span data-ttu-id="d3361-119">Identyfikator istniejącego dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="d3361-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="d3361-120">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="d3361-120">This parameter is required.</span></span>

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

### <span data-ttu-id="d3361-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d3361-121">-Confirm</span></span>
<span data-ttu-id="d3361-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3361-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3361-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3361-123">-WhatIf</span></span>
<span data-ttu-id="d3361-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3361-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3361-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d3361-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3361-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3361-126">CommonParameters</span></span>
<span data-ttu-id="d3361-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3361-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3361-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3361-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3361-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3361-129">INPUTS</span></span>

### <span data-ttu-id="d3361-130">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d3361-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d3361-131">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="d3361-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="d3361-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d3361-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d3361-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d3361-133">OUTPUTS</span></span>

### <span data-ttu-id="d3361-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d3361-134">System.Boolean</span></span>

## <span data-ttu-id="d3361-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d3361-135">NOTES</span></span>

## <span data-ttu-id="d3361-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3361-136">RELATED LINKS</span></span>

[<span data-ttu-id="d3361-137">Nowe — AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="d3361-137">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="d3361-138">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="d3361-138">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="d3361-139">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="d3361-139">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)

