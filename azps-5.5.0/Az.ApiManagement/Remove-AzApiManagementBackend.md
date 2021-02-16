---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
ms.openlocfilehash: 073b32936be1e1614e495ca680a250498742ba66
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199739"
---
# <span data-ttu-id="ad35d-101">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ad35d-101">Remove-AzApiManagementBackend</span></span>

## <span data-ttu-id="ad35d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad35d-102">SYNOPSIS</span></span>
<span data-ttu-id="ad35d-103">Usuwa zaplecza.</span><span class="sxs-lookup"><span data-stu-id="ad35d-103">Removes a Backend.</span></span>

## <span data-ttu-id="ad35d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ad35d-104">SYNTAX</span></span>

```
Remove-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad35d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ad35d-105">DESCRIPTION</span></span>
<span data-ttu-id="ad35d-106">Usuwa backend określony przez identyfikator z zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="ad35d-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="ad35d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ad35d-107">EXAMPLES</span></span>

### <span data-ttu-id="ad35d-108">Przykład 1. Usuwanie bazy danych Backend 123</span><span class="sxs-lookup"><span data-stu-id="ad35d-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="ad35d-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad35d-109">PARAMETERS</span></span>

### <span data-ttu-id="ad35d-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="ad35d-110">-BackendId</span></span>
<span data-ttu-id="ad35d-111">Identyfikator istniejącej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ad35d-111">Identifier of existing backend.</span></span>
<span data-ttu-id="ad35d-112">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="ad35d-112">This parameter is required.</span></span>

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

### <span data-ttu-id="ad35d-113">— kontekst</span><span class="sxs-lookup"><span data-stu-id="ad35d-113">-Context</span></span>
<span data-ttu-id="ad35d-114">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ad35d-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ad35d-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="ad35d-115">This parameter is required.</span></span>

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

### <span data-ttu-id="ad35d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad35d-116">-DefaultProfile</span></span>
<span data-ttu-id="ad35d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad35d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad35d-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad35d-118">-PassThru</span></span>
<span data-ttu-id="ad35d-119">Jeśli zostanie określona, na wypadek, gdyby operacja zakończyła się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="ad35d-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="ad35d-120">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="ad35d-120">This parameter is optional.</span></span>
<span data-ttu-id="ad35d-121">Wartość domyślna to fałsz.</span><span class="sxs-lookup"><span data-stu-id="ad35d-121">Default value is false.</span></span>

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

### <span data-ttu-id="ad35d-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad35d-122">-Confirm</span></span>
<span data-ttu-id="ad35d-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ad35d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad35d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad35d-124">-WhatIf</span></span>
<span data-ttu-id="ad35d-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad35d-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad35d-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ad35d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad35d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad35d-127">CommonParameters</span></span>
<span data-ttu-id="ad35d-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad35d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad35d-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad35d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad35d-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad35d-130">INPUTS</span></span>

### <span data-ttu-id="ad35d-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ad35d-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ad35d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ad35d-132">System.String</span></span>

### <span data-ttu-id="ad35d-133">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="ad35d-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ad35d-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ad35d-134">OUTPUTS</span></span>

### <span data-ttu-id="ad35d-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ad35d-135">System.Boolean</span></span>

## <span data-ttu-id="ad35d-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ad35d-136">NOTES</span></span>

## <span data-ttu-id="ad35d-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad35d-137">RELATED LINKS</span></span>

[<span data-ttu-id="ad35d-138">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ad35d-138">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="ad35d-139">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ad35d-139">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="ad35d-140">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="ad35d-140">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="ad35d-141">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="ad35d-141">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="ad35d-142">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ad35d-142">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)
