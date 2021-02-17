---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
ms.openlocfilehash: 35a6731848c7695a8c649d344abaf466437a34f9
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401587"
---
# <span data-ttu-id="73600-101">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="73600-101">Remove-AzApiManagementBackend</span></span>

## <span data-ttu-id="73600-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73600-102">SYNOPSIS</span></span>
<span data-ttu-id="73600-103">Usuwa zaplecza.</span><span class="sxs-lookup"><span data-stu-id="73600-103">Removes a Backend.</span></span>

## <span data-ttu-id="73600-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="73600-104">SYNTAX</span></span>

```
Remove-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73600-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="73600-105">DESCRIPTION</span></span>
<span data-ttu-id="73600-106">Usuwa backend określony przez identyfikator z zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="73600-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="73600-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="73600-107">EXAMPLES</span></span>

### <span data-ttu-id="73600-108">Przykład 1. Usuwanie bazy danych Backend 123</span><span class="sxs-lookup"><span data-stu-id="73600-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="73600-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73600-109">PARAMETERS</span></span>

### <span data-ttu-id="73600-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="73600-110">-BackendId</span></span>
<span data-ttu-id="73600-111">Identyfikator istniejącej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="73600-111">Identifier of existing backend.</span></span>
<span data-ttu-id="73600-112">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="73600-112">This parameter is required.</span></span>

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

### <span data-ttu-id="73600-113">— kontekst</span><span class="sxs-lookup"><span data-stu-id="73600-113">-Context</span></span>
<span data-ttu-id="73600-114">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="73600-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="73600-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="73600-115">This parameter is required.</span></span>

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

### <span data-ttu-id="73600-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73600-116">-DefaultProfile</span></span>
<span data-ttu-id="73600-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="73600-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73600-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73600-118">-PassThru</span></span>
<span data-ttu-id="73600-119">Jeśli zostanie określona, w przypadku gdy operacja zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="73600-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="73600-120">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="73600-120">This parameter is optional.</span></span>
<span data-ttu-id="73600-121">Wartość domyślna to fałsz.</span><span class="sxs-lookup"><span data-stu-id="73600-121">Default value is false.</span></span>

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

### <span data-ttu-id="73600-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="73600-122">-Confirm</span></span>
<span data-ttu-id="73600-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="73600-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73600-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73600-124">-WhatIf</span></span>
<span data-ttu-id="73600-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73600-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73600-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="73600-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73600-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73600-127">CommonParameters</span></span>
<span data-ttu-id="73600-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73600-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73600-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73600-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73600-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73600-130">INPUTS</span></span>

### <span data-ttu-id="73600-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="73600-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="73600-132">System.String</span><span class="sxs-lookup"><span data-stu-id="73600-132">System.String</span></span>

### <span data-ttu-id="73600-133">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="73600-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="73600-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="73600-134">OUTPUTS</span></span>

### <span data-ttu-id="73600-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="73600-135">System.Boolean</span></span>

## <span data-ttu-id="73600-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="73600-136">NOTES</span></span>

## <span data-ttu-id="73600-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73600-137">RELATED LINKS</span></span>

[<span data-ttu-id="73600-138">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="73600-138">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="73600-139">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="73600-139">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="73600-140">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="73600-140">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="73600-141">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="73600-141">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="73600-142">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="73600-142">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)
