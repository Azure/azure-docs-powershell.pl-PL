---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
ms.openlocfilehash: 3a725bf8dedec948277fac69be029375c3ab91a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710634"
---
# <span data-ttu-id="72d45-101">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="72d45-101">Remove-AzApiManagementBackend</span></span>

## <span data-ttu-id="72d45-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="72d45-102">SYNOPSIS</span></span>
<span data-ttu-id="72d45-103">Usuwanie wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="72d45-103">Removes a Backend.</span></span>

## <span data-ttu-id="72d45-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="72d45-104">SYNTAX</span></span>

```
Remove-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72d45-105">Opis</span><span class="sxs-lookup"><span data-stu-id="72d45-105">DESCRIPTION</span></span>
<span data-ttu-id="72d45-106">Umożliwia usunięcie wewnętrznej bazy danych określonej przez identyfikator z funkcji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="72d45-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="72d45-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="72d45-107">EXAMPLES</span></span>

### <span data-ttu-id="72d45-108">Przykład 1: usunięcie wewnętrznej bazy danych 123</span><span class="sxs-lookup"><span data-stu-id="72d45-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="72d45-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="72d45-109">PARAMETERS</span></span>

### <span data-ttu-id="72d45-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="72d45-110">-BackendId</span></span>
<span data-ttu-id="72d45-111">Identyfikator istniejącej wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="72d45-111">Identifier of existing backend.</span></span>
<span data-ttu-id="72d45-112">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="72d45-112">This parameter is required.</span></span>

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

### <span data-ttu-id="72d45-113">-Context</span><span class="sxs-lookup"><span data-stu-id="72d45-113">-Context</span></span>
<span data-ttu-id="72d45-114">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="72d45-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="72d45-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="72d45-115">This parameter is required.</span></span>

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

### <span data-ttu-id="72d45-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72d45-116">-DefaultProfile</span></span>
<span data-ttu-id="72d45-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="72d45-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72d45-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72d45-118">-PassThru</span></span>
<span data-ttu-id="72d45-119">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="72d45-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="72d45-120">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="72d45-120">This parameter is optional.</span></span>
<span data-ttu-id="72d45-121">Wartość domyślna to false.</span><span class="sxs-lookup"><span data-stu-id="72d45-121">Default value is false.</span></span>

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

### <span data-ttu-id="72d45-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="72d45-122">-Confirm</span></span>
<span data-ttu-id="72d45-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72d45-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72d45-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72d45-124">-WhatIf</span></span>
<span data-ttu-id="72d45-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72d45-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72d45-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="72d45-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72d45-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72d45-127">CommonParameters</span></span>
<span data-ttu-id="72d45-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72d45-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72d45-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72d45-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72d45-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72d45-130">INPUTS</span></span>

### <span data-ttu-id="72d45-131">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="72d45-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="72d45-132">System. String</span><span class="sxs-lookup"><span data-stu-id="72d45-132">System.String</span></span>

### <span data-ttu-id="72d45-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="72d45-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="72d45-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="72d45-134">OUTPUTS</span></span>

### <span data-ttu-id="72d45-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="72d45-135">System.Boolean</span></span>

## <span data-ttu-id="72d45-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="72d45-136">NOTES</span></span>

## <span data-ttu-id="72d45-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72d45-137">RELATED LINKS</span></span>

[<span data-ttu-id="72d45-138">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="72d45-138">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="72d45-139">Nowe — AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="72d45-139">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="72d45-140">Nowe — AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="72d45-140">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="72d45-141">Nowe — AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="72d45-141">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="72d45-142">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="72d45-142">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)
