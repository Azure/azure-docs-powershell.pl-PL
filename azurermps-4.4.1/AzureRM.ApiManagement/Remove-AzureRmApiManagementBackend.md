---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
ms.openlocfilehash: 03f56a17d038407b3a33c09188c9a29b6f4caf09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528358"
---
# <span data-ttu-id="2f4b3-101">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2f4b3-101">Remove-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="2f4b3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2f4b3-102">SYNOPSIS</span></span>
<span data-ttu-id="2f4b3-103">Usuwanie wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2f4b3-103">Removes a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f4b3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2f4b3-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f4b3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2f4b3-105">DESCRIPTION</span></span>
<span data-ttu-id="2f4b3-106">Umożliwia usunięcie wewnętrznej bazy danych określonej przez identyfikator z funkcji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="2f4b3-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="2f4b3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2f4b3-107">EXAMPLES</span></span>

### <span data-ttu-id="2f4b3-108">Przykład 1: usunięcie wewnętrznej bazy danych 123</span><span class="sxs-lookup"><span data-stu-id="2f4b3-108">Example 1: Remove the Backend 123</span></span>
```
Remove-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="2f4b3-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2f4b3-109">PARAMETERS</span></span>

### <span data-ttu-id="2f4b3-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="2f4b3-110">-BackendId</span></span>
<span data-ttu-id="2f4b3-111">Identyfikator istniejącej wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2f4b3-111">Identifier of existing backend.</span></span>
<span data-ttu-id="2f4b3-112">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="2f4b3-112">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f4b3-113">-Context</span><span class="sxs-lookup"><span data-stu-id="2f4b3-113">-Context</span></span>
<span data-ttu-id="2f4b3-114">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2f4b3-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2f4b3-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="2f4b3-115">This parameter is required.</span></span>

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

### <span data-ttu-id="2f4b3-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f4b3-116">-PassThru</span></span>
<span data-ttu-id="2f4b3-117">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="2f4b3-117">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="2f4b3-118">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="2f4b3-118">This parameter is optional.</span></span>
<span data-ttu-id="2f4b3-119">Wartość domyślna to false.</span><span class="sxs-lookup"><span data-stu-id="2f4b3-119">Default value is false.</span></span>

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

### <span data-ttu-id="2f4b3-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2f4b3-120">-Confirm</span></span>
<span data-ttu-id="2f4b3-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f4b3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f4b3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f4b3-122">-WhatIf</span></span>
<span data-ttu-id="2f4b3-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f4b3-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f4b3-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2f4b3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f4b3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f4b3-125">-DefaultProfile</span></span>
<span data-ttu-id="2f4b3-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2f4b3-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f4b3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f4b3-127">CommonParameters</span></span>
<span data-ttu-id="2f4b3-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f4b3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f4b3-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f4b3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f4b3-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f4b3-130">INPUTS</span></span>

## <span data-ttu-id="2f4b3-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2f4b3-131">OUTPUTS</span></span>

### <span data-ttu-id="2f4b3-132">logiczną</span><span class="sxs-lookup"><span data-stu-id="2f4b3-132">bool</span></span>

## <span data-ttu-id="2f4b3-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2f4b3-133">NOTES</span></span>

## <span data-ttu-id="2f4b3-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f4b3-134">RELATED LINKS</span></span>

[<span data-ttu-id="2f4b3-135">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2f4b3-135">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="2f4b3-136">Nowe — AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2f4b3-136">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="2f4b3-137">Nowe — AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="2f4b3-137">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="2f4b3-138">Nowe — AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="2f4b3-138">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="2f4b3-139">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2f4b3-139">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)
