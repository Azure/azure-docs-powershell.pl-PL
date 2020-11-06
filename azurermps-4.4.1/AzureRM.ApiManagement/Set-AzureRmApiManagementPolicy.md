---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 8073df3946f5bf42ee8b0e5f2c7ae7881e905eaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547172"
---
# <span data-ttu-id="ff333-101">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ff333-101">Set-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="ff333-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ff333-102">SYNOPSIS</span></span>
<span data-ttu-id="ff333-103">Ustawia określone zasady dotyczące zakresu zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="ff333-103">Sets the specified scope policy for API Management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff333-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ff333-104">SYNTAX</span></span>

### <span data-ttu-id="ff333-105">Poziom dzierżawy (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="ff333-105">Tenant level (Default)</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff333-106">Poziom produktu</span><span class="sxs-lookup"><span data-stu-id="ff333-106">Product level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ff333-107">Poziom interfejsu API</span><span class="sxs-lookup"><span data-stu-id="ff333-107">API level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ff333-108">Poziom operacji</span><span class="sxs-lookup"><span data-stu-id="ff333-108">Operation level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff333-109">Opis</span><span class="sxs-lookup"><span data-stu-id="ff333-109">DESCRIPTION</span></span>
<span data-ttu-id="ff333-110">Polecenie cmdlet **Set-AzureRmApiManagementPolicy** ustawia określone zasady dotyczące zakresu zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="ff333-110">The **Set-AzureRmApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="ff333-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ff333-111">EXAMPLES</span></span>

### <span data-ttu-id="ff333-112">Przykład 1: Ustawianie zasad na poziomie dzierżawy</span><span class="sxs-lookup"><span data-stu-id="ff333-112">Example 1: Set the tenant level policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="ff333-113">To polecenie ustawia zasady na poziomie dzierżawy na podstawie pliku o nazwie tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="ff333-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="ff333-114">Przykład 2: Ustawianie zasad dotyczących zakresu produktów</span><span class="sxs-lookup"><span data-stu-id="ff333-114">Example 2: Set a product-scope policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="ff333-115">To polecenie ustawia zasady dotyczące zakresu zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="ff333-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="ff333-116">Przykład 3: Ustawianie zasad dotyczących zakresu interfejsów API</span><span class="sxs-lookup"><span data-stu-id="ff333-116">Example 3: Set API-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="ff333-117">To polecenie ustawia zasady dotyczące zakresu interfejsów API dla zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="ff333-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="ff333-118">Przykład 4: Ustawianie zasad dotyczących zakresu operacji</span><span class="sxs-lookup"><span data-stu-id="ff333-118">Example 4: Set operation-scope policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="ff333-119">To polecenie ustawia zasady dotyczące zakresu operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="ff333-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="ff333-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ff333-120">PARAMETERS</span></span>

### <span data-ttu-id="ff333-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ff333-121">-ApiId</span></span>
<span data-ttu-id="ff333-122">Określa identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="ff333-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="ff333-123">W przypadku określenia tego parametru polecenie cmdlet ustawia zasady dotyczące zakresu API.</span><span class="sxs-lookup"><span data-stu-id="ff333-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

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

### <span data-ttu-id="ff333-124">-Context</span><span class="sxs-lookup"><span data-stu-id="ff333-124">-Context</span></span>
<span data-ttu-id="ff333-125">Określa wystąpienie **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="ff333-125">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="ff333-126">-Format</span><span class="sxs-lookup"><span data-stu-id="ff333-126">-Format</span></span>
<span data-ttu-id="ff333-127">Określa format zasad.</span><span class="sxs-lookup"><span data-stu-id="ff333-127">Specifies the format of the policy.</span></span>
<span data-ttu-id="ff333-128">Wartość domyślna to "application/vnd. MS-Azure-APIM. Policy + XML".</span><span class="sxs-lookup"><span data-stu-id="ff333-128">The default value is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="ff333-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="ff333-129">-OperationId</span></span>
<span data-ttu-id="ff333-130">Określa identyfikator istniejącej operacji.</span><span class="sxs-lookup"><span data-stu-id="ff333-130">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="ff333-131">Jeśli określono za pomocą ApiId, ustawi zasady zakresu operacji.</span><span class="sxs-lookup"><span data-stu-id="ff333-131">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="ff333-132">Te parametry są wymagane.</span><span class="sxs-lookup"><span data-stu-id="ff333-132">This parameters is required.</span></span>

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

### <span data-ttu-id="ff333-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff333-133">-PassThru</span></span>
<span data-ttu-id="ff333-134">passthru</span><span class="sxs-lookup"><span data-stu-id="ff333-134">passthru</span></span>

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

### <span data-ttu-id="ff333-135">-Policy</span><span class="sxs-lookup"><span data-stu-id="ff333-135">-Policy</span></span>
<span data-ttu-id="ff333-136">Określa dokument zasad jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="ff333-136">Specifies the policy document as a string.</span></span>
<span data-ttu-id="ff333-137">Ten parametr jest wymagany, jeśli nie podano parametru- *PolicyFilePath* .</span><span class="sxs-lookup"><span data-stu-id="ff333-137">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="ff333-138">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="ff333-138">-PolicyFilePath</span></span>
<span data-ttu-id="ff333-139">Określa ścieżkę pliku dokumentu zasad.</span><span class="sxs-lookup"><span data-stu-id="ff333-139">Specifies the policy document file path.</span></span>
<span data-ttu-id="ff333-140">Ten parametr jest wymagany, jeśli nie określono parametru *Policy* .</span><span class="sxs-lookup"><span data-stu-id="ff333-140">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="ff333-141">-ProductId</span><span class="sxs-lookup"><span data-stu-id="ff333-141">-ProductId</span></span>
<span data-ttu-id="ff333-142">Określa identyfikator istniejącego produktu.</span><span class="sxs-lookup"><span data-stu-id="ff333-142">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="ff333-143">Jeśli ten parametr jest określony, polecenie cmdlet ustawia zasady dotyczące zakresu produktów.</span><span class="sxs-lookup"><span data-stu-id="ff333-143">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

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

### <span data-ttu-id="ff333-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff333-144">-DefaultProfile</span></span>
<span data-ttu-id="ff333-145">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ff333-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff333-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff333-146">CommonParameters</span></span>
<span data-ttu-id="ff333-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff333-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff333-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff333-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff333-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff333-149">INPUTS</span></span>

## <span data-ttu-id="ff333-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ff333-150">OUTPUTS</span></span>

### <span data-ttu-id="ff333-151">logiczną</span><span class="sxs-lookup"><span data-stu-id="ff333-151">bool</span></span>

## <span data-ttu-id="ff333-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ff333-152">NOTES</span></span>

## <span data-ttu-id="ff333-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff333-153">RELATED LINKS</span></span>

[<span data-ttu-id="ff333-154">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ff333-154">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="ff333-155">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ff333-155">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)


