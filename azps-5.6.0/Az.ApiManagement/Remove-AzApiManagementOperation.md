---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
ms.openlocfilehash: 0db56d65893c9c003261c2004435c5d231c014f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990592"
---
# <span data-ttu-id="2b4a0-101">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="2b4a0-101">Remove-AzApiManagementOperation</span></span>

## <span data-ttu-id="2b4a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b4a0-102">SYNOPSIS</span></span>
<span data-ttu-id="2b4a0-103">Usuwa istniejącą operację.</span><span class="sxs-lookup"><span data-stu-id="2b4a0-103">Removes an existing operation.</span></span>

## <span data-ttu-id="2b4a0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2b4a0-104">SYNTAX</span></span>

```
Remove-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b4a0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2b4a0-105">DESCRIPTION</span></span>
<span data-ttu-id="2b4a0-106">Polecenie **cmdlet Remove-AzApiManagementOperation** usuwa istniejącą operację.</span><span class="sxs-lookup"><span data-stu-id="2b4a0-106">The **Remove-AzApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="2b4a0-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2b4a0-107">EXAMPLES</span></span>

### <span data-ttu-id="2b4a0-108">Przykład 1. Usuwanie istniejącej operacji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="2b4a0-108">Example 1: Remove an existing API Operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="2b4a0-109">To polecenie usuwa istniejącą operację interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="2b4a0-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="2b4a0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b4a0-110">PARAMETERS</span></span>

### <span data-ttu-id="2b4a0-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="2b4a0-111">-ApiId</span></span>
<span data-ttu-id="2b4a0-112">Określa identyfikator interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="2b4a0-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="2b4a0-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="2b4a0-113">-ApiRevision</span></span>
<span data-ttu-id="2b4a0-114">Identyfikator poprawki interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="2b4a0-114">Identifier of API Revision.</span></span> <span data-ttu-id="2b4a0-115">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="2b4a0-115">This parameter is optional.</span></span> <span data-ttu-id="2b4a0-116">Jeśli nie zostanie określona, operacja zostanie usunięta z aktualnie aktywnej poprawki interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="2b4a0-116">If not specified, the operation will be removed from the currently active api revision.</span></span>

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

### <span data-ttu-id="2b4a0-117">— kontekst</span><span class="sxs-lookup"><span data-stu-id="2b4a0-117">-Context</span></span>
<span data-ttu-id="2b4a0-118">Określa wystąpienie obiektu **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="2b4a0-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="2b4a0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b4a0-119">-DefaultProfile</span></span>
<span data-ttu-id="2b4a0-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2b4a0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b4a0-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="2b4a0-121">-OperationId</span></span>
<span data-ttu-id="2b4a0-122">Określa identyfikator operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="2b4a0-122">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="2b4a0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b4a0-123">-PassThru</span></span>
<span data-ttu-id="2b4a0-124">Wskazuje, że to polecenie cmdlet zwraca wartość $True się powiedzie, lub wartość $False w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="2b4a0-124">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="2b4a0-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2b4a0-125">-Confirm</span></span>
<span data-ttu-id="2b4a0-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2b4a0-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b4a0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b4a0-127">-WhatIf</span></span>
<span data-ttu-id="2b4a0-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b4a0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b4a0-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2b4a0-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b4a0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b4a0-130">CommonParameters</span></span>
<span data-ttu-id="2b4a0-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b4a0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b4a0-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b4a0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b4a0-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b4a0-133">INPUTS</span></span>

### <span data-ttu-id="2b4a0-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2b4a0-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2b4a0-135">System.String</span><span class="sxs-lookup"><span data-stu-id="2b4a0-135">System.String</span></span>

### <span data-ttu-id="2b4a0-136">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="2b4a0-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2b4a0-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b4a0-137">OUTPUTS</span></span>

### <span data-ttu-id="2b4a0-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2b4a0-138">System.Boolean</span></span>

## <span data-ttu-id="2b4a0-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2b4a0-139">NOTES</span></span>

## <span data-ttu-id="2b4a0-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b4a0-140">RELATED LINKS</span></span>

[<span data-ttu-id="2b4a0-141">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="2b4a0-141">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="2b4a0-142">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="2b4a0-142">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="2b4a0-143">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="2b4a0-143">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


