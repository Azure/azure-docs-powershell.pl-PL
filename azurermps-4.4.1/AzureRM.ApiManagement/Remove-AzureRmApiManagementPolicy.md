---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 5f7fa78cb368afe3e277661122682f43f885f7f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525778"
---
# <span data-ttu-id="12b56-101">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="12b56-101">Remove-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="12b56-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="12b56-102">SYNOPSIS</span></span>
<span data-ttu-id="12b56-103">Usuwa zasady zarządzania interfejsem API z określonego zakresu.</span><span class="sxs-lookup"><span data-stu-id="12b56-103">Removes the API Management policy from a specified scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12b56-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="12b56-104">SYNTAX</span></span>

### <span data-ttu-id="12b56-105">Poziom dzierżawy (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="12b56-105">Tenant level (Default)</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12b56-106">Poziom produktu</span><span class="sxs-lookup"><span data-stu-id="12b56-106">Product level</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12b56-107">Poziom interfejsu API</span><span class="sxs-lookup"><span data-stu-id="12b56-107">API level</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12b56-108">Poziom operacji</span><span class="sxs-lookup"><span data-stu-id="12b56-108">Operation level</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12b56-109">Opis</span><span class="sxs-lookup"><span data-stu-id="12b56-109">DESCRIPTION</span></span>
<span data-ttu-id="12b56-110">Polecenie cmdlet **Remove-AzureRmApiManagementPolicy** usuwa zasady zarządzania interfejsem API z określonego zakresu.</span><span class="sxs-lookup"><span data-stu-id="12b56-110">The **Remove-AzureRmApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="12b56-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="12b56-111">EXAMPLES</span></span>

### <span data-ttu-id="12b56-112">Przykład 1: usuwanie zasad na poziomie dzierżawy</span><span class="sxs-lookup"><span data-stu-id="12b56-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext
```

<span data-ttu-id="12b56-113">To polecenie usuwa zasady dotyczące poziomu dzierżawy z zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="12b56-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="12b56-114">Przykład 2: usunięcie zasad dotyczących zakresu produktów</span><span class="sxs-lookup"><span data-stu-id="12b56-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789"
```

<span data-ttu-id="12b56-115">To polecenie umożliwia usunięcie zasad dotyczących zakresu produktów z funkcji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="12b56-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="12b56-116">Przykład 3: usunięcie zasad dotyczących zakresu interfejsów API</span><span class="sxs-lookup"><span data-stu-id="12b56-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210"
```

<span data-ttu-id="12b56-117">To polecenie usuwa zasady zakresu interfejsów API z zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="12b56-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="12b56-118">Przykład 4: usuwanie zasad dotyczących zakresu operacji</span><span class="sxs-lookup"><span data-stu-id="12b56-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="12b56-119">To polecenie usuwa zasady zakresu operacji z zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="12b56-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="12b56-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12b56-120">PARAMETERS</span></span>

### <span data-ttu-id="12b56-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="12b56-121">-ApiId</span></span>
<span data-ttu-id="12b56-122">Określa identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="12b56-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="12b56-123">Jeśli określisz ten parametr, polecenie cmdlet usunie zasadę zakresu API.</span><span class="sxs-lookup"><span data-stu-id="12b56-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: API level, Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12b56-124">-Context</span><span class="sxs-lookup"><span data-stu-id="12b56-124">-Context</span></span>
<span data-ttu-id="12b56-125">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="12b56-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="12b56-126">-OperationId</span><span class="sxs-lookup"><span data-stu-id="12b56-126">-OperationId</span></span>
<span data-ttu-id="12b56-127">Określa identyfikator istniejącej operacji.</span><span class="sxs-lookup"><span data-stu-id="12b56-127">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="12b56-128">Jeśli określisz ten parametr za pomocą parametru *ApiId* , to polecenie cmdlet spowoduje usunięcie zasad dotyczących zakresu operacji.</span><span class="sxs-lookup"><span data-stu-id="12b56-128">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12b56-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12b56-129">-PassThru</span></span>
<span data-ttu-id="12b56-130">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli się powiodło, lub wartość $False w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="12b56-130">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="12b56-131">-ProductId</span><span class="sxs-lookup"><span data-stu-id="12b56-131">-ProductId</span></span>
<span data-ttu-id="12b56-132">Określa identyfikator istniejącego produktu.</span><span class="sxs-lookup"><span data-stu-id="12b56-132">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="12b56-133">W przypadku określenia tego parametru polecenie cmdlet usuwa zasady dotyczące zakresu produktów.</span><span class="sxs-lookup"><span data-stu-id="12b56-133">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: Product level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12b56-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="12b56-134">-Confirm</span></span>
<span data-ttu-id="12b56-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12b56-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12b56-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12b56-136">-WhatIf</span></span>
<span data-ttu-id="12b56-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12b56-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12b56-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="12b56-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12b56-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12b56-139">-DefaultProfile</span></span>
<span data-ttu-id="12b56-140">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="12b56-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12b56-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12b56-141">CommonParameters</span></span>
<span data-ttu-id="12b56-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12b56-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12b56-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12b56-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12b56-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12b56-144">INPUTS</span></span>

## <span data-ttu-id="12b56-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="12b56-145">OUTPUTS</span></span>

### <span data-ttu-id="12b56-146">Wartość</span><span class="sxs-lookup"><span data-stu-id="12b56-146">Boolean</span></span>

## <span data-ttu-id="12b56-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="12b56-147">NOTES</span></span>

## <span data-ttu-id="12b56-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12b56-148">RELATED LINKS</span></span>

[<span data-ttu-id="12b56-149">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="12b56-149">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="12b56-150">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="12b56-150">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


