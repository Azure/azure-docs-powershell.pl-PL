---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
ms.openlocfilehash: e68fec8bf38dc990737f11d5dc3ed079d71fd6ef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178042"
---
# <span data-ttu-id="9afcc-101">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="9afcc-101">Remove-AzApiManagementLogger</span></span>

## <span data-ttu-id="9afcc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9afcc-102">SYNOPSIS</span></span>
<span data-ttu-id="9afcc-103">Usuwa Loglogię zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="9afcc-103">Removes an API Management Logger.</span></span>

## <span data-ttu-id="9afcc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9afcc-104">SYNTAX</span></span>

```
Remove-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9afcc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9afcc-105">DESCRIPTION</span></span>
<span data-ttu-id="9afcc-106">Polecenie **cmdlet Remove-AzApiManagementLog usuwa** **Loglogowanie** zarządzania interfejsem API platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9afcc-106">The **Remove-AzApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="9afcc-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9afcc-107">EXAMPLES</span></span>

### <span data-ttu-id="9afcc-108">Przykład 1. Usuwanie rejestratora</span><span class="sxs-lookup"><span data-stu-id="9afcc-108">Example 1: Remove a logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="9afcc-109">To polecenie usuwa rejestratora, który ma identyfikator Informacje123.</span><span class="sxs-lookup"><span data-stu-id="9afcc-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="9afcc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9afcc-110">PARAMETERS</span></span>

### <span data-ttu-id="9afcc-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="9afcc-111">-Context</span></span>
<span data-ttu-id="9afcc-112">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="9afcc-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9afcc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9afcc-113">-DefaultProfile</span></span>
<span data-ttu-id="9afcc-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9afcc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9afcc-115">-LogId</span><span class="sxs-lookup"><span data-stu-id="9afcc-115">-LoggerId</span></span>
<span data-ttu-id="9afcc-116">Określa identyfikator loglogii do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="9afcc-116">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="9afcc-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9afcc-117">-PassThru</span></span>
<span data-ttu-id="9afcc-118">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli operacja się powiedzie lub $False w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="9afcc-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="9afcc-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9afcc-119">-Confirm</span></span>
<span data-ttu-id="9afcc-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9afcc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9afcc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9afcc-121">-WhatIf</span></span>
<span data-ttu-id="9afcc-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9afcc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9afcc-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9afcc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9afcc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9afcc-124">CommonParameters</span></span>
<span data-ttu-id="9afcc-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9afcc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9afcc-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9afcc-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9afcc-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9afcc-127">INPUTS</span></span>

### <span data-ttu-id="9afcc-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9afcc-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9afcc-129">System.String</span><span class="sxs-lookup"><span data-stu-id="9afcc-129">System.String</span></span>

### <span data-ttu-id="9afcc-130">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="9afcc-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9afcc-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9afcc-131">OUTPUTS</span></span>

### <span data-ttu-id="9afcc-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9afcc-132">System.Boolean</span></span>

## <span data-ttu-id="9afcc-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9afcc-133">NOTES</span></span>

## <span data-ttu-id="9afcc-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9afcc-134">RELATED LINKS</span></span>

[<span data-ttu-id="9afcc-135">Get-AzApiManagement Jednakowy</span><span class="sxs-lookup"><span data-stu-id="9afcc-135">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="9afcc-136">New-AzApiManagement Jednakowy</span><span class="sxs-lookup"><span data-stu-id="9afcc-136">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="9afcc-137">Set-AzApiManagement Jednakowy</span><span class="sxs-lookup"><span data-stu-id="9afcc-137">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


