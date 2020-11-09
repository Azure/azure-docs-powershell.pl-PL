---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
ms.openlocfilehash: 153eb354ae8ba0f033a34010658b0d851572ddd6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319369"
---
# <span data-ttu-id="57764-101">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="57764-101">Remove-AzApiManagementOperation</span></span>

## <span data-ttu-id="57764-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="57764-102">SYNOPSIS</span></span>
<span data-ttu-id="57764-103">Usuwa istniejącą operację.</span><span class="sxs-lookup"><span data-stu-id="57764-103">Removes an existing operation.</span></span>

## <span data-ttu-id="57764-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="57764-104">SYNTAX</span></span>

```
Remove-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57764-105">Opis</span><span class="sxs-lookup"><span data-stu-id="57764-105">DESCRIPTION</span></span>
<span data-ttu-id="57764-106">Polecenie cmdlet **Remove-AzApiManagementOperation** Usuwa istniejącą operację.</span><span class="sxs-lookup"><span data-stu-id="57764-106">The **Remove-AzApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="57764-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="57764-107">EXAMPLES</span></span>

### <span data-ttu-id="57764-108">Przykład 1. Usuń istniejącą operację interfejsu API</span><span class="sxs-lookup"><span data-stu-id="57764-108">Example 1: Remove an existing API Operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="57764-109">To polecenie usuwa istniejącą operację interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="57764-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="57764-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="57764-110">PARAMETERS</span></span>

### <span data-ttu-id="57764-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="57764-111">-ApiId</span></span>
<span data-ttu-id="57764-112">Określa identyfikator interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="57764-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="57764-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="57764-113">-ApiRevision</span></span>
<span data-ttu-id="57764-114">Identyfikator wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="57764-114">Identifier of API Revision.</span></span> <span data-ttu-id="57764-115">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="57764-115">This parameter is optional.</span></span> <span data-ttu-id="57764-116">Jeśli nie określono tej funkcji, operacja zostanie usunięta z bieżącej aktywnej wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="57764-116">If not specified, the operation will be removed from the currently active api revision.</span></span>

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

### <span data-ttu-id="57764-117">-Context</span><span class="sxs-lookup"><span data-stu-id="57764-117">-Context</span></span>
<span data-ttu-id="57764-118">Określa wystąpienie **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="57764-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="57764-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57764-119">-DefaultProfile</span></span>
<span data-ttu-id="57764-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="57764-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57764-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="57764-121">-OperationId</span></span>
<span data-ttu-id="57764-122">Określa identyfikator operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="57764-122">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="57764-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57764-123">-PassThru</span></span>
<span data-ttu-id="57764-124">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli ta operacja się powiedzie lub wartość $False w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="57764-124">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="57764-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="57764-125">-Confirm</span></span>
<span data-ttu-id="57764-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57764-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57764-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57764-127">-WhatIf</span></span>
<span data-ttu-id="57764-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57764-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57764-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="57764-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57764-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57764-130">CommonParameters</span></span>
<span data-ttu-id="57764-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57764-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57764-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57764-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57764-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57764-133">INPUTS</span></span>

### <span data-ttu-id="57764-134">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="57764-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="57764-135">System. String</span><span class="sxs-lookup"><span data-stu-id="57764-135">System.String</span></span>

### <span data-ttu-id="57764-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="57764-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="57764-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="57764-137">OUTPUTS</span></span>

### <span data-ttu-id="57764-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="57764-138">System.Boolean</span></span>

## <span data-ttu-id="57764-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="57764-139">NOTES</span></span>

## <span data-ttu-id="57764-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57764-140">RELATED LINKS</span></span>

[<span data-ttu-id="57764-141">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="57764-141">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="57764-142">Nowe — AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="57764-142">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="57764-143">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="57764-143">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


