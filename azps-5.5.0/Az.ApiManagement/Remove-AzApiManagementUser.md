---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
ms.openlocfilehash: 4c90b51a316db63bad2e5481e1b6390849d83292
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178034"
---
# <span data-ttu-id="d5a67-101">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="d5a67-101">Remove-AzApiManagementUser</span></span>

## <span data-ttu-id="d5a67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5a67-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a67-103">Usuwa istniejącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d5a67-103">Deletes an existing user.</span></span>

## <span data-ttu-id="d5a67-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d5a67-104">SYNTAX</span></span>

```
Remove-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5a67-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d5a67-105">DESCRIPTION</span></span>
<span data-ttu-id="d5a67-106">Polecenie **cmdlet Remove-AzApiManagementUser** usuwa istniejącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d5a67-106">The **Remove-AzApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="d5a67-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d5a67-107">EXAMPLES</span></span>

### <span data-ttu-id="d5a67-108">Przykład 1. Usuwanie użytkownika</span><span class="sxs-lookup"><span data-stu-id="d5a67-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="d5a67-109">To polecenie usuwa istniejącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d5a67-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="d5a67-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5a67-110">PARAMETERS</span></span>

### <span data-ttu-id="d5a67-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="d5a67-111">-Context</span></span>
<span data-ttu-id="d5a67-112">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="d5a67-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="d5a67-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="d5a67-113">This parameter is required.</span></span>

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

### <span data-ttu-id="d5a67-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5a67-114">-DefaultProfile</span></span>
<span data-ttu-id="d5a67-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5a67-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5a67-116">- DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="d5a67-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="d5a67-117">Wskazuje, czy chcesz usunąć subskrypcje produktu.</span><span class="sxs-lookup"><span data-stu-id="d5a67-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="d5a67-118">Jeśli ten parametr nie jest określony i istnieje subskrypcja, to polecenie cmdlet zgłasza wyjątek.</span><span class="sxs-lookup"><span data-stu-id="d5a67-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="d5a67-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d5a67-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="d5a67-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5a67-120">-PassThru</span></span>
<span data-ttu-id="d5a67-121">Wskazuje, że to polecenie cmdlet zwraca wartość $Ture, jeśli się powiedzie, lub wartość $False w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="d5a67-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="d5a67-122">-UserId</span><span class="sxs-lookup"><span data-stu-id="d5a67-122">-UserId</span></span>
<span data-ttu-id="d5a67-123">Określa identyfikator użytkownika do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="d5a67-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="d5a67-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d5a67-124">-Confirm</span></span>
<span data-ttu-id="d5a67-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d5a67-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5a67-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5a67-126">-WhatIf</span></span>
<span data-ttu-id="d5a67-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5a67-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5a67-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d5a67-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5a67-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a67-129">CommonParameters</span></span>
<span data-ttu-id="d5a67-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5a67-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a67-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5a67-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a67-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5a67-132">INPUTS</span></span>

### <span data-ttu-id="d5a67-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d5a67-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d5a67-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d5a67-134">System.String</span></span>

### <span data-ttu-id="d5a67-135">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="d5a67-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d5a67-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d5a67-136">OUTPUTS</span></span>

### <span data-ttu-id="d5a67-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d5a67-137">System.Boolean</span></span>

## <span data-ttu-id="d5a67-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d5a67-138">NOTES</span></span>

## <span data-ttu-id="d5a67-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5a67-139">RELATED LINKS</span></span>

[<span data-ttu-id="d5a67-140">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="d5a67-140">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="d5a67-141">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="d5a67-141">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="d5a67-142">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="d5a67-142">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


