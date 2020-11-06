---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
ms.openlocfilehash: ef00a5140dc25065c05494211721c5773a9b5243
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524717"
---
# <span data-ttu-id="41498-101">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="41498-101">Remove-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="41498-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41498-102">SYNOPSIS</span></span>
<span data-ttu-id="41498-103">Usuwanie wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="41498-103">Removes a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41498-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41498-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41498-105">Opis</span><span class="sxs-lookup"><span data-stu-id="41498-105">DESCRIPTION</span></span>
<span data-ttu-id="41498-106">Umożliwia usunięcie wewnętrznej bazy danych określonej przez identyfikator z funkcji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="41498-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="41498-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41498-107">EXAMPLES</span></span>

### <span data-ttu-id="41498-108">Przykład 1: usunięcie wewnętrznej bazy danych 123</span><span class="sxs-lookup"><span data-stu-id="41498-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="41498-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41498-109">PARAMETERS</span></span>

### <span data-ttu-id="41498-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="41498-110">-BackendId</span></span>
<span data-ttu-id="41498-111">Identyfikator istniejącej wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="41498-111">Identifier of existing backend.</span></span>
<span data-ttu-id="41498-112">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="41498-112">This parameter is required.</span></span>

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

### <span data-ttu-id="41498-113">-Context</span><span class="sxs-lookup"><span data-stu-id="41498-113">-Context</span></span>
<span data-ttu-id="41498-114">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="41498-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="41498-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="41498-115">This parameter is required.</span></span>

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

### <span data-ttu-id="41498-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41498-116">-DefaultProfile</span></span>
<span data-ttu-id="41498-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="41498-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41498-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41498-118">-PassThru</span></span>
<span data-ttu-id="41498-119">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="41498-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="41498-120">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="41498-120">This parameter is optional.</span></span>
<span data-ttu-id="41498-121">Wartość domyślna to false.</span><span class="sxs-lookup"><span data-stu-id="41498-121">Default value is false.</span></span>

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

### <span data-ttu-id="41498-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="41498-122">-Confirm</span></span>
<span data-ttu-id="41498-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41498-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41498-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41498-124">-WhatIf</span></span>
<span data-ttu-id="41498-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41498-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41498-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="41498-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41498-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41498-127">CommonParameters</span></span>
<span data-ttu-id="41498-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41498-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41498-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41498-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41498-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41498-130">INPUTS</span></span>

### <span data-ttu-id="41498-131">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="41498-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="41498-132">System. String</span><span class="sxs-lookup"><span data-stu-id="41498-132">System.String</span></span>

### <span data-ttu-id="41498-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="41498-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="41498-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41498-134">OUTPUTS</span></span>

### <span data-ttu-id="41498-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="41498-135">System.Boolean</span></span>

## <span data-ttu-id="41498-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41498-136">NOTES</span></span>

## <span data-ttu-id="41498-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41498-137">RELATED LINKS</span></span>

[<span data-ttu-id="41498-138">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="41498-138">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="41498-139">Nowe — AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="41498-139">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="41498-140">Nowe — AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="41498-140">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="41498-141">Nowe — AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="41498-141">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="41498-142">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="41498-142">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)
