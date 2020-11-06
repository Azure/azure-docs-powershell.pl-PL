---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
ms.openlocfilehash: 31ab005953ea405dc8aac093f973a6e842974814
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550392"
---
# <span data-ttu-id="5afc0-101">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="5afc0-101">Remove-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="5afc0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5afc0-102">SYNOPSIS</span></span>
<span data-ttu-id="5afc0-103">Usuwa istniejącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="5afc0-103">Deletes an existing user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5afc0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5afc0-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5afc0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5afc0-105">DESCRIPTION</span></span>
<span data-ttu-id="5afc0-106">Polecenie cmdlet **Remove-AzureRmApiManagementUser** Usuwa istniejącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="5afc0-106">The **Remove-AzureRmApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="5afc0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5afc0-107">EXAMPLES</span></span>

### <span data-ttu-id="5afc0-108">Przykład 1: Usuwanie użytkownika</span><span class="sxs-lookup"><span data-stu-id="5afc0-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="5afc0-109">To polecenie usuwa istniejącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="5afc0-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="5afc0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5afc0-110">PARAMETERS</span></span>

### <span data-ttu-id="5afc0-111">-Context</span><span class="sxs-lookup"><span data-stu-id="5afc0-111">-Context</span></span>
<span data-ttu-id="5afc0-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="5afc0-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="5afc0-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="5afc0-113">This parameter is required.</span></span>

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

### <span data-ttu-id="5afc0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5afc0-114">-DefaultProfile</span></span>
<span data-ttu-id="5afc0-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5afc0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5afc0-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="5afc0-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="5afc0-117">Wskazuje, czy należy usunąć abonamenty do produktu.</span><span class="sxs-lookup"><span data-stu-id="5afc0-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="5afc0-118">Jeśli ten parametr nie zostanie określony i istnieje subskrypcja, to polecenie cmdlet zgłosi wyjątek.</span><span class="sxs-lookup"><span data-stu-id="5afc0-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="5afc0-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="5afc0-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="5afc0-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5afc0-120">-PassThru</span></span>
<span data-ttu-id="5afc0-121">Wskazuje, że to polecenie cmdlet zwraca wartość $Ture, jeśli się powiodło, lub wartość $False w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="5afc0-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="5afc0-122">-UserId</span><span class="sxs-lookup"><span data-stu-id="5afc0-122">-UserId</span></span>
<span data-ttu-id="5afc0-123">Określa identyfikator użytkownika, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="5afc0-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="5afc0-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5afc0-124">-Confirm</span></span>
<span data-ttu-id="5afc0-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5afc0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5afc0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5afc0-126">-WhatIf</span></span>
<span data-ttu-id="5afc0-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5afc0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5afc0-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5afc0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5afc0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5afc0-129">CommonParameters</span></span>
<span data-ttu-id="5afc0-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5afc0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5afc0-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5afc0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5afc0-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5afc0-132">INPUTS</span></span>

### <span data-ttu-id="5afc0-133">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5afc0-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5afc0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5afc0-134">System.String</span></span>

### <span data-ttu-id="5afc0-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5afc0-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5afc0-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5afc0-136">OUTPUTS</span></span>

### <span data-ttu-id="5afc0-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5afc0-137">System.Boolean</span></span>

## <span data-ttu-id="5afc0-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5afc0-138">NOTES</span></span>

## <span data-ttu-id="5afc0-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5afc0-139">RELATED LINKS</span></span>

[<span data-ttu-id="5afc0-140">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="5afc0-140">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="5afc0-141">Nowe — AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="5afc0-141">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="5afc0-142">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="5afc0-142">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


