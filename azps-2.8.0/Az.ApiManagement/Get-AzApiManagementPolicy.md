---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
ms.openlocfilehash: fa065aa7e56572fbcb58fd78a3feff4a0909be9c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707066"
---
# <span data-ttu-id="63204-101">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="63204-101">Get-AzApiManagementPolicy</span></span>

## <span data-ttu-id="63204-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="63204-102">SYNOPSIS</span></span>
<span data-ttu-id="63204-103">Pobiera określone zasady dotyczące zakresu.</span><span class="sxs-lookup"><span data-stu-id="63204-103">Gets the specified scope policy.</span></span>

## <span data-ttu-id="63204-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="63204-104">SYNTAX</span></span>

### <span data-ttu-id="63204-105">GetTenantLevel (domyślny)</span><span class="sxs-lookup"><span data-stu-id="63204-105">GetTenantLevel (Default)</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63204-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="63204-106">GetProductLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63204-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="63204-107">GetApiLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63204-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="63204-108">GetOperationLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] -OperationId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63204-109">Opis</span><span class="sxs-lookup"><span data-stu-id="63204-109">DESCRIPTION</span></span>
<span data-ttu-id="63204-110">Polecenie cmdlet **Get-AzApiManagementPolicy** pobiera określone zasady dotyczące zakresu.</span><span class="sxs-lookup"><span data-stu-id="63204-110">The **Get-AzApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="63204-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="63204-111">EXAMPLES</span></span>

### <span data-ttu-id="63204-112">Przykład 1: uzyskiwanie zasad na poziomie dzierżawy</span><span class="sxs-lookup"><span data-stu-id="63204-112">Example 1: Get the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="63204-113">To polecenie pobiera zasady na poziomie dzierżawy i zapisuje je w pliku o nazwie tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="63204-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="63204-114">Przykład 2: uzyskiwanie zasad dotyczących zakresu produktów</span><span class="sxs-lookup"><span data-stu-id="63204-114">Example 2: Get the product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="63204-115">To polecenie uzyskuje zasady dotyczące zakresu produktów</span><span class="sxs-lookup"><span data-stu-id="63204-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="63204-116">Przykład 3: uzyskiwanie zasad dotyczących zakresu interfejsów API</span><span class="sxs-lookup"><span data-stu-id="63204-116">Example 3: Get the API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="63204-117">To polecenie pobiera zasady dotyczące zakresu interfejsów API.</span><span class="sxs-lookup"><span data-stu-id="63204-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="63204-118">Przykład 4: uzyskiwanie zasad dotyczących zakresu operacji</span><span class="sxs-lookup"><span data-stu-id="63204-118">Example 4: Get the operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="63204-119">To polecenie uzyskuje zasady dotyczące zakresu operacji.</span><span class="sxs-lookup"><span data-stu-id="63204-119">This command gets the operation-scope policy.</span></span>

### <span data-ttu-id="63204-120">Przykład 5: uzyskiwanie zasad dotyczących zakresu dzierżaw w formacie RawXml</span><span class="sxs-lookup"><span data-stu-id="63204-120">Example 5: Get the Tenant scope policy in RawXml format</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS c:\> Get-AzApiManagementPolicy -Context $context -Format rawxml

<policies>
        <inbound>
                <set-header name="correlationid" exists-action="skip">
                        <value>@{
                var guidBinary = new byte[16];
                Array.Copy(Guid.NewGuid().ToByteArray(), 0, guidBinary, 0, 10);
                long time = DateTime.Now.Ticks;
                byte[] bytes = new byte[6];
                unchecked
                {
                       bytes[5] = (byte)(time >> 40);
                       bytes[4] = (byte)(time >> 32);
                       bytes[3] = (byte)(time >> 24);
                       bytes[2] = (byte)(time >> 16);
                       bytes[1] = (byte)(time >> 8);
                       bytes[0] = (byte)(time);
                }
                Array.Copy(bytes, 0, guidBinary, 10, 6);
                return new Guid(guidBinary).ToString();
            }
            </value>
                </set-header>
        </inbound>
        <backend>
                <forward-request />
        </backend>
        <outbound />
        <on-error />
</policies>
```

<span data-ttu-id="63204-121">To polecenie pobiera zasady dotyczące zakresu dzierżawy w formacie innym niż XML.</span><span class="sxs-lookup"><span data-stu-id="63204-121">This command gets the tenant-scope policy in Non-Xml escaped format.</span></span>

## <span data-ttu-id="63204-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="63204-122">PARAMETERS</span></span>

### <span data-ttu-id="63204-123">-ApiId</span><span class="sxs-lookup"><span data-stu-id="63204-123">-ApiId</span></span>
<span data-ttu-id="63204-124">Określa identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="63204-124">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="63204-125">W przypadku określenia tego parametru polecenie cmdlet zwraca zasadę zakresu API.</span><span class="sxs-lookup"><span data-stu-id="63204-125">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63204-126">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="63204-126">-ApiRevision</span></span>
<span data-ttu-id="63204-127">Identyfikator wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="63204-127">Identifier of API Revision.</span></span> <span data-ttu-id="63204-128">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="63204-128">This parameter is optional.</span></span> <span data-ttu-id="63204-129">Jeśli ta pozycja nie jest określona, zasady zostaną pobrane z wersji obecnie aktywnej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="63204-129">If not specified, the policy will be retrieved from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63204-130">-Context</span><span class="sxs-lookup"><span data-stu-id="63204-130">-Context</span></span>
<span data-ttu-id="63204-131">Określa wystąpienie **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="63204-131">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="63204-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63204-132">-DefaultProfile</span></span>
<span data-ttu-id="63204-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="63204-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63204-134">-Force</span><span class="sxs-lookup"><span data-stu-id="63204-134">-Force</span></span>
<span data-ttu-id="63204-135">ps_force</span><span class="sxs-lookup"><span data-stu-id="63204-135">ps_force</span></span>

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

### <span data-ttu-id="63204-136">-Format</span><span class="sxs-lookup"><span data-stu-id="63204-136">-Format</span></span>
<span data-ttu-id="63204-137">Określa format zasad zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="63204-137">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="63204-138">Domyślną wartością tego parametru jest "XML".</span><span class="sxs-lookup"><span data-stu-id="63204-138">The default value for this parameter is "xml".</span></span>

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

### <span data-ttu-id="63204-139">-OperationId</span><span class="sxs-lookup"><span data-stu-id="63204-139">-OperationId</span></span>
<span data-ttu-id="63204-140">Określa identyfikator istniejącej operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="63204-140">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="63204-141">Jeśli określisz ten parametr za pomocą funkcji *ApiId* , polecenie cmdlet zwraca zasady zakresu operacja.</span><span class="sxs-lookup"><span data-stu-id="63204-141">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63204-142">-ProductId</span><span class="sxs-lookup"><span data-stu-id="63204-142">-ProductId</span></span>
<span data-ttu-id="63204-143">Określa identyfikator istniejącego produktu.</span><span class="sxs-lookup"><span data-stu-id="63204-143">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="63204-144">W przypadku określenia tego parametru polecenie cmdlet zwraca zasadę zakresu produktu.</span><span class="sxs-lookup"><span data-stu-id="63204-144">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63204-145">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="63204-145">-SaveAs</span></span>
<span data-ttu-id="63204-146">Określa ścieżkę pliku, do którego ma zostać zapisany wynik.</span><span class="sxs-lookup"><span data-stu-id="63204-146">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="63204-147">Jeśli nie określisz tego parametru, wynik jest przestawny jako Sting.</span><span class="sxs-lookup"><span data-stu-id="63204-147">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="63204-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="63204-148">-Confirm</span></span>
<span data-ttu-id="63204-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63204-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63204-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63204-150">-WhatIf</span></span>
<span data-ttu-id="63204-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63204-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63204-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="63204-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63204-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63204-153">CommonParameters</span></span>
<span data-ttu-id="63204-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63204-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63204-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63204-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63204-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63204-156">INPUTS</span></span>

### <span data-ttu-id="63204-157">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="63204-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="63204-158">System. String</span><span class="sxs-lookup"><span data-stu-id="63204-158">System.String</span></span>

### <span data-ttu-id="63204-159">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="63204-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="63204-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="63204-160">OUTPUTS</span></span>

### <span data-ttu-id="63204-161">System. String</span><span class="sxs-lookup"><span data-stu-id="63204-161">System.String</span></span>

## <span data-ttu-id="63204-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="63204-162">NOTES</span></span>

## <span data-ttu-id="63204-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63204-163">RELATED LINKS</span></span>

[<span data-ttu-id="63204-164">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="63204-164">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)

[<span data-ttu-id="63204-165">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="63204-165">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)

