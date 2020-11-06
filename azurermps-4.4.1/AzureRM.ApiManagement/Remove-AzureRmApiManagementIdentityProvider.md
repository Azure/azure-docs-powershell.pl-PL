---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: ecbb2b6671f1482f31cb7b3f0b07d4e9be4bbb3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528350"
---
# <span data-ttu-id="2ca94-101">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2ca94-101">Remove-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="2ca94-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2ca94-102">SYNOPSIS</span></span>
<span data-ttu-id="2ca94-103">Usuwa istniejącą konfigurację dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="2ca94-103">Removes an existing Identity Provider Configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ca94-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2ca94-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ca94-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2ca94-105">DESCRIPTION</span></span>
<span data-ttu-id="2ca94-106">Usuwa istniejącą konfigurację dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="2ca94-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="2ca94-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2ca94-107">EXAMPLES</span></span>

### <span data-ttu-id="2ca94-108">Usuwa ustawienia dostawcy tożsamości w serwisie Facebook z usługi ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2ca94-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
Remove-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="2ca94-109">Usuwa konfigurację dotyczącą konfiguracji dostawcy tożsamości w serwisie Facebook.</span><span class="sxs-lookup"><span data-stu-id="2ca94-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="2ca94-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2ca94-110">PARAMETERS</span></span>

### <span data-ttu-id="2ca94-111">-Context</span><span class="sxs-lookup"><span data-stu-id="2ca94-111">-Context</span></span>
<span data-ttu-id="2ca94-112">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2ca94-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2ca94-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="2ca94-113">This parameter is required.</span></span>

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

### <span data-ttu-id="2ca94-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ca94-114">-PassThru</span></span>
<span data-ttu-id="2ca94-115">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli operacja się powiedzie lub $False w inny sposób.</span><span class="sxs-lookup"><span data-stu-id="2ca94-115">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>


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

### <span data-ttu-id="2ca94-116">-Type</span><span class="sxs-lookup"><span data-stu-id="2ca94-116">-Type</span></span>
<span data-ttu-id="2ca94-117">Identyfikator istniejącego dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="2ca94-117">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="2ca94-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="2ca94-118">This parameter is required.</span></span>

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

### <span data-ttu-id="2ca94-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2ca94-119">-Confirm</span></span>
<span data-ttu-id="2ca94-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ca94-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ca94-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ca94-121">-WhatIf</span></span>
<span data-ttu-id="2ca94-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ca94-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ca94-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2ca94-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ca94-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ca94-124">-DefaultProfile</span></span>
<span data-ttu-id="2ca94-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ca94-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ca94-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ca94-126">CommonParameters</span></span>
<span data-ttu-id="2ca94-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ca94-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ca94-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ca94-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ca94-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ca94-129">INPUTS</span></span>

## <span data-ttu-id="2ca94-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2ca94-130">OUTPUTS</span></span>

### <span data-ttu-id="2ca94-131">logiczną</span><span class="sxs-lookup"><span data-stu-id="2ca94-131">bool</span></span>

## <span data-ttu-id="2ca94-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2ca94-132">NOTES</span></span>

## <span data-ttu-id="2ca94-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ca94-133">RELATED LINKS</span></span>

[<span data-ttu-id="2ca94-134">Nowe — AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2ca94-134">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="2ca94-135">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2ca94-135">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="2ca94-136">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2ca94-136">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)

