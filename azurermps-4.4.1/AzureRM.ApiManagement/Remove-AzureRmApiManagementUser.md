---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
ms.openlocfilehash: 6be4c714627d77b0e3c56b8dd9766c550deebd7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525749"
---
# <span data-ttu-id="64322-101">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="64322-101">Remove-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="64322-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="64322-102">SYNOPSIS</span></span>
<span data-ttu-id="64322-103">Usuwa istniejącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="64322-103">Deletes an existing user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64322-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="64322-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64322-105">Opis</span><span class="sxs-lookup"><span data-stu-id="64322-105">DESCRIPTION</span></span>
<span data-ttu-id="64322-106">Polecenie cmdlet **Remove-AzureRmApiManagementUser** Usuwa istniejącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="64322-106">The **Remove-AzureRmApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="64322-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="64322-107">EXAMPLES</span></span>

### <span data-ttu-id="64322-108">Przykład 1: Usuwanie użytkownika</span><span class="sxs-lookup"><span data-stu-id="64322-108">Example 1: Delete a user</span></span>
```
PS C:\>Remove-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="64322-109">To polecenie usuwa istniejącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="64322-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="64322-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="64322-110">PARAMETERS</span></span>

### <span data-ttu-id="64322-111">-Context</span><span class="sxs-lookup"><span data-stu-id="64322-111">-Context</span></span>
<span data-ttu-id="64322-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="64322-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="64322-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="64322-113">This parameter is required.</span></span>

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

### <span data-ttu-id="64322-114">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="64322-114">-DeleteSubscriptions</span></span>
<span data-ttu-id="64322-115">Wskazuje, czy należy usunąć abonamenty do produktu.</span><span class="sxs-lookup"><span data-stu-id="64322-115">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="64322-116">Jeśli ten parametr nie zostanie określony i istnieje subskrypcja, to polecenie cmdlet zgłosi wyjątek.</span><span class="sxs-lookup"><span data-stu-id="64322-116">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="64322-117">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="64322-117">This parameter is optional.</span></span>

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

### <span data-ttu-id="64322-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64322-118">-PassThru</span></span>
<span data-ttu-id="64322-119">Wskazuje, że to polecenie cmdlet zwraca wartość $Ture, jeśli się powiodło, lub wartość $False w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="64322-119">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="64322-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="64322-120">-UserId</span></span>
<span data-ttu-id="64322-121">Określa identyfikator użytkownika, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="64322-121">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="64322-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="64322-122">-Confirm</span></span>
<span data-ttu-id="64322-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64322-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64322-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64322-124">-WhatIf</span></span>
<span data-ttu-id="64322-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64322-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64322-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="64322-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64322-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64322-127">-DefaultProfile</span></span>
<span data-ttu-id="64322-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="64322-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64322-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64322-129">CommonParameters</span></span>
<span data-ttu-id="64322-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64322-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64322-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64322-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64322-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64322-132">INPUTS</span></span>

## <span data-ttu-id="64322-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="64322-133">OUTPUTS</span></span>

### <span data-ttu-id="64322-134">Wartość</span><span class="sxs-lookup"><span data-stu-id="64322-134">Boolean</span></span>

## <span data-ttu-id="64322-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="64322-135">NOTES</span></span>

## <span data-ttu-id="64322-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64322-136">RELATED LINKS</span></span>

[<span data-ttu-id="64322-137">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="64322-137">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="64322-138">Nowe — AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="64322-138">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="64322-139">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="64322-139">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


