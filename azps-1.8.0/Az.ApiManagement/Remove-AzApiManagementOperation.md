---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
ms.openlocfilehash: 6c44ff9fe0c96dc3b87540493f11864b2441d340
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869419"
---
# <span data-ttu-id="b873c-101">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="b873c-101">Remove-AzApiManagementOperation</span></span>

## <span data-ttu-id="b873c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b873c-102">SYNOPSIS</span></span>
<span data-ttu-id="b873c-103">Usuwa istniejącą operację.</span><span class="sxs-lookup"><span data-stu-id="b873c-103">Removes an existing operation.</span></span>

## <span data-ttu-id="b873c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b873c-104">SYNTAX</span></span>

```
Remove-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b873c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b873c-105">DESCRIPTION</span></span>
<span data-ttu-id="b873c-106">Polecenie cmdlet **Remove-AzApiManagementOperation** Usuwa istniejącą operację.</span><span class="sxs-lookup"><span data-stu-id="b873c-106">The **Remove-AzApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="b873c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b873c-107">EXAMPLES</span></span>

### <span data-ttu-id="b873c-108">Przykład 1. Usuń istniejącą operację interfejsu API</span><span class="sxs-lookup"><span data-stu-id="b873c-108">Example 1: Remove an existing API Operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="b873c-109">To polecenie usuwa istniejącą operację interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b873c-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="b873c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b873c-110">PARAMETERS</span></span>

### <span data-ttu-id="b873c-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="b873c-111">-ApiId</span></span>
<span data-ttu-id="b873c-112">Określa identyfikator interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b873c-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="b873c-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="b873c-113">-ApiRevision</span></span>
<span data-ttu-id="b873c-114">Identyfikator wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b873c-114">Identifier of API Revision.</span></span> <span data-ttu-id="b873c-115">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b873c-115">This parameter is optional.</span></span> <span data-ttu-id="b873c-116">Jeśli nie określono tej funkcji, operacja zostanie usunięta z bieżącej aktywnej wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b873c-116">If not specified, the operation will be removed from the currently active api revision.</span></span>

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

### <span data-ttu-id="b873c-117">-Context</span><span class="sxs-lookup"><span data-stu-id="b873c-117">-Context</span></span>
<span data-ttu-id="b873c-118">Określa wystąpienie **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="b873c-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="b873c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b873c-119">-DefaultProfile</span></span>
<span data-ttu-id="b873c-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b873c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b873c-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="b873c-121">-OperationId</span></span>
<span data-ttu-id="b873c-122">Określa identyfikator operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b873c-122">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="b873c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b873c-123">-PassThru</span></span>
<span data-ttu-id="b873c-124">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli ta operacja się powiedzie lub wartość $False w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="b873c-124">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="b873c-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b873c-125">-Confirm</span></span>
<span data-ttu-id="b873c-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b873c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b873c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b873c-127">-WhatIf</span></span>
<span data-ttu-id="b873c-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b873c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b873c-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b873c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b873c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b873c-130">CommonParameters</span></span>
<span data-ttu-id="b873c-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b873c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b873c-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b873c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b873c-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b873c-133">INPUTS</span></span>

### <span data-ttu-id="b873c-134">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b873c-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b873c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b873c-135">System.String</span></span>

### <span data-ttu-id="b873c-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b873c-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b873c-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b873c-137">OUTPUTS</span></span>

### <span data-ttu-id="b873c-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b873c-138">System.Boolean</span></span>

## <span data-ttu-id="b873c-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b873c-139">NOTES</span></span>

## <span data-ttu-id="b873c-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b873c-140">RELATED LINKS</span></span>

[<span data-ttu-id="b873c-141">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="b873c-141">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="b873c-142">Nowe — AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="b873c-142">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="b873c-143">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="b873c-143">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


