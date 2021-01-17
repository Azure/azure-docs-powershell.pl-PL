---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
ms.openlocfilehash: a51bd7aed5ca8793a921c2cde7729c5280df44b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382011"
---
# <span data-ttu-id="99b00-101">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="99b00-101">Remove-AzApiManagementPolicy</span></span>

## <span data-ttu-id="99b00-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="99b00-102">SYNOPSIS</span></span>
<span data-ttu-id="99b00-103">Usuwa zasady zarządzania interfejsem API z określonego zakresu.</span><span class="sxs-lookup"><span data-stu-id="99b00-103">Removes the API Management policy from a specified scope.</span></span>

## <span data-ttu-id="99b00-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="99b00-104">SYNTAX</span></span>

### <span data-ttu-id="99b00-105">RemoveTenantLevel (domyślny)</span><span class="sxs-lookup"><span data-stu-id="99b00-105">RemoveTenantLevel (Default)</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99b00-106">RemoveProductLevel</span><span class="sxs-lookup"><span data-stu-id="99b00-106">RemoveProductLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99b00-107">RemoveApiLevel</span><span class="sxs-lookup"><span data-stu-id="99b00-107">RemoveApiLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99b00-108">RemoveOperationLevel</span><span class="sxs-lookup"><span data-stu-id="99b00-108">RemoveOperationLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99b00-109">Opis</span><span class="sxs-lookup"><span data-stu-id="99b00-109">DESCRIPTION</span></span>
<span data-ttu-id="99b00-110">Polecenie cmdlet **Remove-AzApiManagementPolicy** usuwa zasady zarządzania interfejsem API z określonego zakresu.</span><span class="sxs-lookup"><span data-stu-id="99b00-110">The **Remove-AzApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="99b00-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="99b00-111">EXAMPLES</span></span>

### <span data-ttu-id="99b00-112">Przykład 1: usuwanie zasad na poziomie dzierżawy</span><span class="sxs-lookup"><span data-stu-id="99b00-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext
```

<span data-ttu-id="99b00-113">To polecenie usuwa zasady dotyczące poziomu dzierżawy z zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="99b00-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="99b00-114">Przykład 2: usunięcie zasad dotyczących zakresu produktów</span><span class="sxs-lookup"><span data-stu-id="99b00-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="99b00-115">To polecenie umożliwia usunięcie zasad dotyczących zakresu produktów z funkcji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="99b00-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="99b00-116">Przykład 3: usunięcie zasad dotyczących zakresu interfejsów API</span><span class="sxs-lookup"><span data-stu-id="99b00-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="99b00-117">To polecenie usuwa zasady zakresu interfejsów API z zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="99b00-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="99b00-118">Przykład 4: usuwanie zasad dotyczących zakresu operacji</span><span class="sxs-lookup"><span data-stu-id="99b00-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="99b00-119">To polecenie usuwa zasady zakresu operacji z zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="99b00-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="99b00-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="99b00-120">PARAMETERS</span></span>

### <span data-ttu-id="99b00-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="99b00-121">-ApiId</span></span>
<span data-ttu-id="99b00-122">Określa identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="99b00-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="99b00-123">Jeśli określisz ten parametr, polecenie cmdlet usunie zasadę zakresu API.</span><span class="sxs-lookup"><span data-stu-id="99b00-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveApiLevel, RemoveOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b00-124">-Context</span><span class="sxs-lookup"><span data-stu-id="99b00-124">-Context</span></span>
<span data-ttu-id="99b00-125">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="99b00-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="99b00-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99b00-126">-DefaultProfile</span></span>
<span data-ttu-id="99b00-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="99b00-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99b00-128">-OperationId</span><span class="sxs-lookup"><span data-stu-id="99b00-128">-OperationId</span></span>
<span data-ttu-id="99b00-129">Określa identyfikator istniejącej operacji.</span><span class="sxs-lookup"><span data-stu-id="99b00-129">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="99b00-130">Jeśli określisz ten parametr za pomocą parametru *ApiId* , to polecenie cmdlet spowoduje usunięcie zasad dotyczących zakresu operacji.</span><span class="sxs-lookup"><span data-stu-id="99b00-130">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b00-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99b00-131">-PassThru</span></span>
<span data-ttu-id="99b00-132">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli się powiodło, lub wartość $False w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="99b00-132">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="99b00-133">-ProductId</span><span class="sxs-lookup"><span data-stu-id="99b00-133">-ProductId</span></span>
<span data-ttu-id="99b00-134">Określa identyfikator istniejącego produktu.</span><span class="sxs-lookup"><span data-stu-id="99b00-134">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="99b00-135">W przypadku określenia tego parametru polecenie cmdlet usuwa zasady dotyczące zakresu produktów.</span><span class="sxs-lookup"><span data-stu-id="99b00-135">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b00-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="99b00-136">-Confirm</span></span>
<span data-ttu-id="99b00-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99b00-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99b00-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99b00-138">-WhatIf</span></span>
<span data-ttu-id="99b00-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99b00-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99b00-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="99b00-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99b00-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99b00-141">CommonParameters</span></span>
<span data-ttu-id="99b00-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99b00-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99b00-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99b00-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99b00-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99b00-144">INPUTS</span></span>

### <span data-ttu-id="99b00-145">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="99b00-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="99b00-146">System. String</span><span class="sxs-lookup"><span data-stu-id="99b00-146">System.String</span></span>

### <span data-ttu-id="99b00-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="99b00-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="99b00-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="99b00-148">OUTPUTS</span></span>

### <span data-ttu-id="99b00-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="99b00-149">System.Boolean</span></span>

## <span data-ttu-id="99b00-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="99b00-150">NOTES</span></span>

## <span data-ttu-id="99b00-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99b00-151">RELATED LINKS</span></span>

[<span data-ttu-id="99b00-152">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="99b00-152">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="99b00-153">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="99b00-153">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


