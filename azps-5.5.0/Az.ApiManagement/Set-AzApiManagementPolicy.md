---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
ms.openlocfilehash: ee0a95653dbc949518c485554c6202664d943ba3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244363"
---
# <span data-ttu-id="c6f43-101">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c6f43-101">Set-AzApiManagementPolicy</span></span>

## <span data-ttu-id="c6f43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6f43-102">SYNOPSIS</span></span>
<span data-ttu-id="c6f43-103">Ustawia określone zasady zakresu dla zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="c6f43-103">Sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="c6f43-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c6f43-104">SYNTAX</span></span>

### <span data-ttu-id="c6f43-105">SetTenantLevel (Default)</span><span class="sxs-lookup"><span data-stu-id="c6f43-105">SetTenantLevel (Default)</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c6f43-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="c6f43-106">SetProductLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6f43-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="c6f43-107">SetApiLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6f43-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="c6f43-108">SetOperationLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>]
 [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6f43-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="c6f43-109">DESCRIPTION</span></span>
<span data-ttu-id="c6f43-110">Polecenie **cmdlet Set-AzApiManagementPolicy** ustawia określone zasady zakresu zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="c6f43-110">The **Set-AzApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="c6f43-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c6f43-111">EXAMPLES</span></span>

### <span data-ttu-id="c6f43-112">Przykład 1. Ustawianie zasad na poziomie dzierżawy</span><span class="sxs-lookup"><span data-stu-id="c6f43-112">Example 1: Set the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="c6f43-113">To polecenie ustawia zasady na poziomie dzierżawy z pliku o nazwie tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="c6f43-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="c6f43-114">Przykład 2. Ustawianie zasad zakresu produktu</span><span class="sxs-lookup"><span data-stu-id="c6f43-114">Example 2: Set a product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="c6f43-115">To polecenie ustawia zasady zakresu produktu dla zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="c6f43-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="c6f43-116">Przykład 3. Ustawianie zasad zakresu interfejsu API</span><span class="sxs-lookup"><span data-stu-id="c6f43-116">Example 3: Set API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="c6f43-117">To polecenie ustawia zasady zakresu interfejsu API dla zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="c6f43-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="c6f43-118">Przykład 4. Ustawianie zasad zakresu operacji</span><span class="sxs-lookup"><span data-stu-id="c6f43-118">Example 4: Set operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="c6f43-119">To polecenie ustawia zasady zakresu operacji dla zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="c6f43-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="c6f43-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6f43-120">PARAMETERS</span></span>

### <span data-ttu-id="c6f43-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c6f43-121">-ApiId</span></span>
<span data-ttu-id="c6f43-122">Określa identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="c6f43-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="c6f43-123">Jeśli określisz ten parametr, polecenie cmdlet ustawia zasady zakresu interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="c6f43-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

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

### <span data-ttu-id="c6f43-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="c6f43-124">-ApiRevision</span></span>
<span data-ttu-id="c6f43-125">Identyfikator poprawki interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="c6f43-125">Identifier of API Revision.</span></span> <span data-ttu-id="c6f43-126">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="c6f43-126">This parameter is optional.</span></span> <span data-ttu-id="c6f43-127">Jeśli nie zostanie określona, zasady zostaną zaktualizowane w aktualnie aktywnej poprawce interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="c6f43-127">If not specified, the policy will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="c6f43-128">— kontekst</span><span class="sxs-lookup"><span data-stu-id="c6f43-128">-Context</span></span>
<span data-ttu-id="c6f43-129">Określa wystąpienie obiektu **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="c6f43-129">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="c6f43-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6f43-130">-DefaultProfile</span></span>
<span data-ttu-id="c6f43-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c6f43-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6f43-132">— Format</span><span class="sxs-lookup"><span data-stu-id="c6f43-132">-Format</span></span>
<span data-ttu-id="c6f43-133">Określa format zasad.</span><span class="sxs-lookup"><span data-stu-id="c6f43-133">Specifies the format of the policy.</span></span> <span data-ttu-id="c6f43-134">W przypadku `application/vnd.ms-azure-apim.policy+xml` używania wyrażeń zawartych w zasadach należy uniknąć kodu XML.</span><span class="sxs-lookup"><span data-stu-id="c6f43-134">When using `application/vnd.ms-azure-apim.policy+xml`, expressions contained within the policy must be XML-escaped.</span></span> <span data-ttu-id="c6f43-135">W przypadku używania zasady nie muszą podlegać `application/vnd.ms-azure-apim.policy.raw+xml` uchybce  w języku XML.</span><span class="sxs-lookup"><span data-stu-id="c6f43-135">When using `application/vnd.ms-azure-apim.policy.raw+xml` it is **not** necessary for the policy to be XML-escaped.</span></span>
<span data-ttu-id="c6f43-136">Wartość domyślna `application/vnd.ms-azure-apim.policy+xml` to.</span><span class="sxs-lookup"><span data-stu-id="c6f43-136">The default value is `application/vnd.ms-azure-apim.policy+xml`.</span></span>
<span data-ttu-id="c6f43-137">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="c6f43-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="c6f43-138">-OperationId</span><span class="sxs-lookup"><span data-stu-id="c6f43-138">-OperationId</span></span>
<span data-ttu-id="c6f43-139">Określa identyfikator istniejącej operacji.</span><span class="sxs-lookup"><span data-stu-id="c6f43-139">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="c6f43-140">Jeśli zostanie określona wartość z wartością ApiId, zostaną ustawione zasady zakresu operacji.</span><span class="sxs-lookup"><span data-stu-id="c6f43-140">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="c6f43-141">Te parametry są wymagane.</span><span class="sxs-lookup"><span data-stu-id="c6f43-141">This parameters is required.</span></span>

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

### <span data-ttu-id="c6f43-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6f43-142">-PassThru</span></span>
<span data-ttu-id="c6f43-143">passthru</span><span class="sxs-lookup"><span data-stu-id="c6f43-143">passthru</span></span>

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

### <span data-ttu-id="c6f43-144">— Zasady</span><span class="sxs-lookup"><span data-stu-id="c6f43-144">-Policy</span></span>
<span data-ttu-id="c6f43-145">Określa dokument zasad jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="c6f43-145">Specifies the policy document as a string.</span></span>
<span data-ttu-id="c6f43-146">Ten parametr jest wymagany, jeśli nie określono parametru -*PolicyFilePath.*</span><span class="sxs-lookup"><span data-stu-id="c6f43-146">This parameter is required if the -*PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="c6f43-147">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="c6f43-147">-PolicyFilePath</span></span>
<span data-ttu-id="c6f43-148">Określa ścieżkę pliku dokumentu zasad.</span><span class="sxs-lookup"><span data-stu-id="c6f43-148">Specifies the policy document file path.</span></span>
<span data-ttu-id="c6f43-149">Ten parametr jest wymagany, *jeśli* parametr Zasady nie został określony.</span><span class="sxs-lookup"><span data-stu-id="c6f43-149">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="c6f43-150">-PolicyUrl</span><span class="sxs-lookup"><span data-stu-id="c6f43-150">-PolicyUrl</span></span>
<span data-ttu-id="c6f43-151">Adres URL, pod którym jest hostowany dokument zasad.</span><span class="sxs-lookup"><span data-stu-id="c6f43-151">The Url where the Policy document is hosted.</span></span> <span data-ttu-id="c6f43-152">Ten parametr jest wymagany, jeśli nie określono parametru -Policy lub -PolicyFilePath.</span><span class="sxs-lookup"><span data-stu-id="c6f43-152">This parameter is required if -Policy or -PolicyFilePath is not specified.</span></span>

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

### <span data-ttu-id="c6f43-153">- ProductId</span><span class="sxs-lookup"><span data-stu-id="c6f43-153">-ProductId</span></span>
<span data-ttu-id="c6f43-154">Określa identyfikator istniejącego produktu.</span><span class="sxs-lookup"><span data-stu-id="c6f43-154">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="c6f43-155">Jeśli ten parametr jest określony, polecenie cmdlet ustawia zasady zakresu produktu.</span><span class="sxs-lookup"><span data-stu-id="c6f43-155">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

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

### <span data-ttu-id="c6f43-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6f43-156">CommonParameters</span></span>
<span data-ttu-id="c6f43-157">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6f43-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6f43-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6f43-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6f43-159">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6f43-159">INPUTS</span></span>

### <span data-ttu-id="c6f43-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c6f43-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c6f43-161">System.String</span><span class="sxs-lookup"><span data-stu-id="c6f43-161">System.String</span></span>

### <span data-ttu-id="c6f43-162">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="c6f43-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c6f43-163">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6f43-163">OUTPUTS</span></span>

### <span data-ttu-id="c6f43-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c6f43-164">System.Boolean</span></span>

## <span data-ttu-id="c6f43-165">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c6f43-165">NOTES</span></span>

## <span data-ttu-id="c6f43-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6f43-166">RELATED LINKS</span></span>

[<span data-ttu-id="c6f43-167">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c6f43-167">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="c6f43-168">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c6f43-168">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)


