---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
ms.openlocfilehash: d9c682f12bd56c2f862396670ce77a8730712279
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706930"
---
# <span data-ttu-id="5ceab-101">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="5ceab-101">Remove-AzApiManagementUser</span></span>

## <span data-ttu-id="5ceab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ceab-102">SYNOPSIS</span></span>
<span data-ttu-id="5ceab-103">Usuwa istniejącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="5ceab-103">Deletes an existing user.</span></span>

## <span data-ttu-id="5ceab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ceab-104">SYNTAX</span></span>

```
Remove-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ceab-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5ceab-105">DESCRIPTION</span></span>
<span data-ttu-id="5ceab-106">Polecenie cmdlet **Remove-AzApiManagementUser** Usuwa istniejącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="5ceab-106">The **Remove-AzApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="5ceab-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ceab-107">EXAMPLES</span></span>

### <span data-ttu-id="5ceab-108">Przykład 1: Usuwanie użytkownika</span><span class="sxs-lookup"><span data-stu-id="5ceab-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="5ceab-109">To polecenie usuwa istniejącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="5ceab-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="5ceab-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ceab-110">PARAMETERS</span></span>

### <span data-ttu-id="5ceab-111">-Context</span><span class="sxs-lookup"><span data-stu-id="5ceab-111">-Context</span></span>
<span data-ttu-id="5ceab-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="5ceab-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="5ceab-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="5ceab-113">This parameter is required.</span></span>

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

### <span data-ttu-id="5ceab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ceab-114">-DefaultProfile</span></span>
<span data-ttu-id="5ceab-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ceab-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ceab-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="5ceab-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="5ceab-117">Wskazuje, czy należy usunąć abonamenty do produktu.</span><span class="sxs-lookup"><span data-stu-id="5ceab-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="5ceab-118">Jeśli ten parametr nie zostanie określony i istnieje subskrypcja, to polecenie cmdlet zgłosi wyjątek.</span><span class="sxs-lookup"><span data-stu-id="5ceab-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="5ceab-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="5ceab-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="5ceab-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ceab-120">-PassThru</span></span>
<span data-ttu-id="5ceab-121">Wskazuje, że to polecenie cmdlet zwraca wartość $Ture, jeśli się powiodło, lub wartość $False w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="5ceab-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="5ceab-122">-UserId</span><span class="sxs-lookup"><span data-stu-id="5ceab-122">-UserId</span></span>
<span data-ttu-id="5ceab-123">Określa identyfikator użytkownika, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="5ceab-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="5ceab-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ceab-124">-Confirm</span></span>
<span data-ttu-id="5ceab-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ceab-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ceab-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ceab-126">-WhatIf</span></span>
<span data-ttu-id="5ceab-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ceab-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ceab-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5ceab-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ceab-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ceab-129">CommonParameters</span></span>
<span data-ttu-id="5ceab-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ceab-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ceab-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ceab-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ceab-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ceab-132">INPUTS</span></span>

### <span data-ttu-id="5ceab-133">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5ceab-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5ceab-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5ceab-134">System.String</span></span>

### <span data-ttu-id="5ceab-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5ceab-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5ceab-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ceab-136">OUTPUTS</span></span>

### <span data-ttu-id="5ceab-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5ceab-137">System.Boolean</span></span>

## <span data-ttu-id="5ceab-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ceab-138">NOTES</span></span>

## <span data-ttu-id="5ceab-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ceab-139">RELATED LINKS</span></span>

[<span data-ttu-id="5ceab-140">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="5ceab-140">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="5ceab-141">Nowe — AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="5ceab-141">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="5ceab-142">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="5ceab-142">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


