---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 0f9ee1c2190dbc3d657ecc52cd85b6af8b0cac4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717130"
---
# <span data-ttu-id="891a8-101">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="891a8-101">Set-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="891a8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="891a8-102">SYNOPSIS</span></span>
<span data-ttu-id="891a8-103">Ustawia określone zasady dotyczące zakresu zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="891a8-103">Sets the specified scope policy for API Management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="891a8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="891a8-104">SYNTAX</span></span>

### <span data-ttu-id="891a8-105">SetTenantLevel (domyślny)</span><span class="sxs-lookup"><span data-stu-id="891a8-105">SetTenantLevel (Default)</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="891a8-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="891a8-106">SetProductLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="891a8-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="891a8-107">SetApiLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="891a8-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="891a8-108">SetOperationLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="891a8-109">Opis</span><span class="sxs-lookup"><span data-stu-id="891a8-109">DESCRIPTION</span></span>
<span data-ttu-id="891a8-110">Polecenie cmdlet **Set-AzureRmApiManagementPolicy** ustawia określone zasady dotyczące zakresu zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="891a8-110">The **Set-AzureRmApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="891a8-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="891a8-111">EXAMPLES</span></span>

### <span data-ttu-id="891a8-112">Przykład 1: Ustawianie zasad na poziomie dzierżawy</span><span class="sxs-lookup"><span data-stu-id="891a8-112">Example 1: Set the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="891a8-113">To polecenie ustawia zasady na poziomie dzierżawy na podstawie pliku o nazwie tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="891a8-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="891a8-114">Przykład 2: Ustawianie zasad dotyczących zakresu produktów</span><span class="sxs-lookup"><span data-stu-id="891a8-114">Example 2: Set a product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="891a8-115">To polecenie ustawia zasady dotyczące zakresu zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="891a8-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="891a8-116">Przykład 3: Ustawianie zasad dotyczących zakresu interfejsów API</span><span class="sxs-lookup"><span data-stu-id="891a8-116">Example 3: Set API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="891a8-117">To polecenie ustawia zasady dotyczące zakresu interfejsów API dla zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="891a8-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="891a8-118">Przykład 4: Ustawianie zasad dotyczących zakresu operacji</span><span class="sxs-lookup"><span data-stu-id="891a8-118">Example 4: Set operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="891a8-119">To polecenie ustawia zasady dotyczące zakresu operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="891a8-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="891a8-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="891a8-120">PARAMETERS</span></span>

### <span data-ttu-id="891a8-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="891a8-121">-ApiId</span></span>
<span data-ttu-id="891a8-122">Określa identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="891a8-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="891a8-123">W przypadku określenia tego parametru polecenie cmdlet ustawia zasady dotyczące zakresu API.</span><span class="sxs-lookup"><span data-stu-id="891a8-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="891a8-124">-Context</span><span class="sxs-lookup"><span data-stu-id="891a8-124">-Context</span></span>
<span data-ttu-id="891a8-125">Określa wystąpienie **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="891a8-125">Specifies the instance of **PsApiManagementContext**.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="891a8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="891a8-126">-DefaultProfile</span></span>
<span data-ttu-id="891a8-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="891a8-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="891a8-128">-Format</span><span class="sxs-lookup"><span data-stu-id="891a8-128">-Format</span></span>
<span data-ttu-id="891a8-129">Określa format zasad.</span><span class="sxs-lookup"><span data-stu-id="891a8-129">Specifies the format of the policy.</span></span>
<span data-ttu-id="891a8-130">Wartość domyślna to "application/vnd. MS-Azure-APIM. Policy + XML".</span><span class="sxs-lookup"><span data-stu-id="891a8-130">The default value is "application/vnd.ms-azure-apim.policy+xml".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="891a8-131">-OperationId</span><span class="sxs-lookup"><span data-stu-id="891a8-131">-OperationId</span></span>
<span data-ttu-id="891a8-132">Określa identyfikator istniejącej operacji.</span><span class="sxs-lookup"><span data-stu-id="891a8-132">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="891a8-133">Jeśli określono za pomocą ApiId, ustawi zasady zakresu operacji.</span><span class="sxs-lookup"><span data-stu-id="891a8-133">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="891a8-134">Te parametry są wymagane.</span><span class="sxs-lookup"><span data-stu-id="891a8-134">This parameters is required.</span></span>

```yaml
Type: String
Parameter Sets: SetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="891a8-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="891a8-135">-PassThru</span></span>
<span data-ttu-id="891a8-136">passthru</span><span class="sxs-lookup"><span data-stu-id="891a8-136">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="891a8-137">-Policy</span><span class="sxs-lookup"><span data-stu-id="891a8-137">-Policy</span></span>
<span data-ttu-id="891a8-138">Określa dokument zasad jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="891a8-138">Specifies the policy document as a string.</span></span>
<span data-ttu-id="891a8-139">Ten parametr jest wymagany, jeśli nie podano parametru- *PolicyFilePath* .</span><span class="sxs-lookup"><span data-stu-id="891a8-139">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="891a8-140">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="891a8-140">-PolicyFilePath</span></span>
<span data-ttu-id="891a8-141">Określa ścieżkę pliku dokumentu zasad.</span><span class="sxs-lookup"><span data-stu-id="891a8-141">Specifies the policy document file path.</span></span>
<span data-ttu-id="891a8-142">Ten parametr jest wymagany, jeśli nie określono parametru *Policy* .</span><span class="sxs-lookup"><span data-stu-id="891a8-142">This parameter is required if the *Policy* parameter is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="891a8-143">-ProductId</span><span class="sxs-lookup"><span data-stu-id="891a8-143">-ProductId</span></span>
<span data-ttu-id="891a8-144">Określa identyfikator istniejącego produktu.</span><span class="sxs-lookup"><span data-stu-id="891a8-144">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="891a8-145">Jeśli ten parametr jest określony, polecenie cmdlet ustawia zasady dotyczące zakresu produktów.</span><span class="sxs-lookup"><span data-stu-id="891a8-145">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: SetProductLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="891a8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="891a8-146">CommonParameters</span></span>
<span data-ttu-id="891a8-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="891a8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="891a8-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="891a8-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="891a8-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="891a8-149">INPUTS</span></span>

### <span data-ttu-id="891a8-150">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="891a8-150">None</span></span>
<span data-ttu-id="891a8-151">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="891a8-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="891a8-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="891a8-152">OUTPUTS</span></span>

### <span data-ttu-id="891a8-153">logiczną</span><span class="sxs-lookup"><span data-stu-id="891a8-153">bool</span></span>

## <span data-ttu-id="891a8-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="891a8-154">NOTES</span></span>

## <span data-ttu-id="891a8-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="891a8-155">RELATED LINKS</span></span>

[<span data-ttu-id="891a8-156">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="891a8-156">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="891a8-157">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="891a8-157">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)


