---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
ms.openlocfilehash: 495e076a58d4cb1f19de4f9b7eb740e14aa7b407
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869328"
---
# <span data-ttu-id="dc590-101">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="dc590-101">Set-AzApiManagementPolicy</span></span>

## <span data-ttu-id="dc590-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dc590-102">SYNOPSIS</span></span>
<span data-ttu-id="dc590-103">Ustawia określone zasady dotyczące zakresu zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="dc590-103">Sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="dc590-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dc590-104">SYNTAX</span></span>

### <span data-ttu-id="dc590-105">SetTenantLevel (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dc590-105">SetTenantLevel (Default)</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc590-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="dc590-106">SetProductLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc590-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="dc590-107">SetApiLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc590-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="dc590-108">SetOperationLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>]
 [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc590-109">Opis</span><span class="sxs-lookup"><span data-stu-id="dc590-109">DESCRIPTION</span></span>
<span data-ttu-id="dc590-110">Polecenie cmdlet **Set-AzApiManagementPolicy** ustawia określone zasady dotyczące zakresu zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="dc590-110">The **Set-AzApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="dc590-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dc590-111">EXAMPLES</span></span>

### <span data-ttu-id="dc590-112">Przykład 1: Ustawianie zasad na poziomie dzierżawy</span><span class="sxs-lookup"><span data-stu-id="dc590-112">Example 1: Set the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="dc590-113">To polecenie ustawia zasady na poziomie dzierżawy na podstawie pliku o nazwie tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="dc590-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="dc590-114">Przykład 2: Ustawianie zasad dotyczących zakresu produktów</span><span class="sxs-lookup"><span data-stu-id="dc590-114">Example 2: Set a product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="dc590-115">To polecenie ustawia zasady dotyczące zakresu zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="dc590-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="dc590-116">Przykład 3: Ustawianie zasad dotyczących zakresu interfejsów API</span><span class="sxs-lookup"><span data-stu-id="dc590-116">Example 3: Set API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="dc590-117">To polecenie ustawia zasady dotyczące zakresu interfejsów API dla zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="dc590-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="dc590-118">Przykład 4: Ustawianie zasad dotyczących zakresu operacji</span><span class="sxs-lookup"><span data-stu-id="dc590-118">Example 4: Set operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="dc590-119">To polecenie ustawia zasady dotyczące zakresu operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="dc590-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="dc590-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dc590-120">PARAMETERS</span></span>

### <span data-ttu-id="dc590-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="dc590-121">-ApiId</span></span>
<span data-ttu-id="dc590-122">Określa identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="dc590-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="dc590-123">W przypadku określenia tego parametru polecenie cmdlet ustawia zasady dotyczące zakresu API.</span><span class="sxs-lookup"><span data-stu-id="dc590-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc590-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="dc590-124">-ApiRevision</span></span>
<span data-ttu-id="dc590-125">Identyfikator wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="dc590-125">Identifier of API Revision.</span></span> <span data-ttu-id="dc590-126">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="dc590-126">This parameter is optional.</span></span> <span data-ttu-id="dc590-127">Jeśli ta pozycja nie jest określona, zasady zostaną zaktualizowane w wersji obecnie aktywnej funkcji API.</span><span class="sxs-lookup"><span data-stu-id="dc590-127">If not specified, the policy will be updated in the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc590-128">-Context</span><span class="sxs-lookup"><span data-stu-id="dc590-128">-Context</span></span>
<span data-ttu-id="dc590-129">Określa wystąpienie **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="dc590-129">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="dc590-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc590-130">-DefaultProfile</span></span>
<span data-ttu-id="dc590-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dc590-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc590-132">-Format</span><span class="sxs-lookup"><span data-stu-id="dc590-132">-Format</span></span>
<span data-ttu-id="dc590-133">Określa format zasad.</span><span class="sxs-lookup"><span data-stu-id="dc590-133">Specifies the format of the policy.</span></span> <span data-ttu-id="dc590-134">W przypadku używania `application/vnd.ms-az-apim.policy+xml` wyrażenia zawarte w zasadach muszą być oparte na formacie XML-Escape.</span><span class="sxs-lookup"><span data-stu-id="dc590-134">When using `application/vnd.ms-az-apim.policy+xml`, expressions contained within the policy must be XML-escaped.</span></span> <span data-ttu-id="dc590-135">W przypadku korzystania z `application/vnd.ms-az-apim.policy.raw+xml` tej zasady **nie** trzeba być XML-Escape.</span><span class="sxs-lookup"><span data-stu-id="dc590-135">When using `application/vnd.ms-az-apim.policy.raw+xml` it is **not** necessary for the policy to be XML-escaped.</span></span>
<span data-ttu-id="dc590-136">Wartość domyślna to `application/vnd.ms-az-apim.policy+xml` .</span><span class="sxs-lookup"><span data-stu-id="dc590-136">The default value is `application/vnd.ms-az-apim.policy+xml`.</span></span>
<span data-ttu-id="dc590-137">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="dc590-137">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: application/vnd.ms-azure-apim.policy.raw+xml, application/vnd.ms-azure-apim.policy+xml

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc590-138">-OperationId</span><span class="sxs-lookup"><span data-stu-id="dc590-138">-OperationId</span></span>
<span data-ttu-id="dc590-139">Określa identyfikator istniejącej operacji.</span><span class="sxs-lookup"><span data-stu-id="dc590-139">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="dc590-140">Jeśli określono za pomocą ApiId, ustawi zasady zakresu operacji.</span><span class="sxs-lookup"><span data-stu-id="dc590-140">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="dc590-141">Te parametry są wymagane.</span><span class="sxs-lookup"><span data-stu-id="dc590-141">This parameters is required.</span></span>

```yaml
Type: System.String
Parameter Sets: SetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc590-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc590-142">-PassThru</span></span>
<span data-ttu-id="dc590-143">passthru</span><span class="sxs-lookup"><span data-stu-id="dc590-143">passthru</span></span>

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

### <span data-ttu-id="dc590-144">-Policy</span><span class="sxs-lookup"><span data-stu-id="dc590-144">-Policy</span></span>
<span data-ttu-id="dc590-145">Określa dokument zasad jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="dc590-145">Specifies the policy document as a string.</span></span>
<span data-ttu-id="dc590-146">Ten parametr jest wymagany, jeśli nie podano parametru- *PolicyFilePath* .</span><span class="sxs-lookup"><span data-stu-id="dc590-146">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="dc590-147">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="dc590-147">-PolicyFilePath</span></span>
<span data-ttu-id="dc590-148">Określa ścieżkę pliku dokumentu zasad.</span><span class="sxs-lookup"><span data-stu-id="dc590-148">Specifies the policy document file path.</span></span>
<span data-ttu-id="dc590-149">Ten parametr jest wymagany, jeśli nie określono parametru *Policy* .</span><span class="sxs-lookup"><span data-stu-id="dc590-149">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="dc590-150">-PolicyUrl</span><span class="sxs-lookup"><span data-stu-id="dc590-150">-PolicyUrl</span></span>
<span data-ttu-id="dc590-151">Adres URL, pod którym znajduje się dokument zasad.</span><span class="sxs-lookup"><span data-stu-id="dc590-151">The Url where the Policy document is hosted.</span></span> <span data-ttu-id="dc590-152">Ten parametr jest wymagany, jeśli nie określono parametru-Policy lub-PolicyFilePath.</span><span class="sxs-lookup"><span data-stu-id="dc590-152">This parameter is required if -Policy or -PolicyFilePath is not specified.</span></span>

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

### <span data-ttu-id="dc590-153">-ProductId</span><span class="sxs-lookup"><span data-stu-id="dc590-153">-ProductId</span></span>
<span data-ttu-id="dc590-154">Określa identyfikator istniejącego produktu.</span><span class="sxs-lookup"><span data-stu-id="dc590-154">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="dc590-155">Jeśli ten parametr jest określony, polecenie cmdlet ustawia zasady dotyczące zakresu produktów.</span><span class="sxs-lookup"><span data-stu-id="dc590-155">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc590-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc590-156">CommonParameters</span></span>
<span data-ttu-id="dc590-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc590-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc590-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc590-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc590-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc590-159">INPUTS</span></span>

### <span data-ttu-id="dc590-160">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dc590-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dc590-161">System. String</span><span class="sxs-lookup"><span data-stu-id="dc590-161">System.String</span></span>

### <span data-ttu-id="dc590-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dc590-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dc590-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dc590-163">OUTPUTS</span></span>

### <span data-ttu-id="dc590-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dc590-164">System.Boolean</span></span>

## <span data-ttu-id="dc590-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dc590-165">NOTES</span></span>

## <span data-ttu-id="dc590-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc590-166">RELATED LINKS</span></span>

[<span data-ttu-id="dc590-167">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="dc590-167">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="dc590-168">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="dc590-168">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)


