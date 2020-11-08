---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
ms.openlocfilehash: 08e29c91e253c648b774e56d7e236accdd5fbff0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063026"
---
# <span data-ttu-id="61037-101">New-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="61037-101">New-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="61037-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="61037-102">SYNOPSIS</span></span>
<span data-ttu-id="61037-103">Tworzy nową nazwaną wartość.</span><span class="sxs-lookup"><span data-stu-id="61037-103">Creates new Named Value.</span></span>

## <span data-ttu-id="61037-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="61037-104">SYNTAX</span></span>

```
New-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61037-105">Opis</span><span class="sxs-lookup"><span data-stu-id="61037-105">DESCRIPTION</span></span>
<span data-ttu-id="61037-106">Polecenie cmdlet **New-AzApiManagementNamedValue** tworzy funkcję zarządzania interfejsem Azure API **o nazwie Value**.</span><span class="sxs-lookup"><span data-stu-id="61037-106">The **New-AzApiManagementNamedValue** cmdlet creates an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="61037-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="61037-107">EXAMPLES</span></span>

### <span data-ttu-id="61037-108">Przykład 1. Tworzenie nazwanej wartości obejmującej znaczniki</span><span class="sxs-lookup"><span data-stu-id="61037-108">Example 1: Create a named value that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="61037-109">Pierwsze polecenie powoduje przypisanie dwóch wartości do zmiennej $Tags.</span><span class="sxs-lookup"><span data-stu-id="61037-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="61037-110">Drugie polecenie tworzy nazwaną wartość i przypisuje ciągi w $Tags jako znaczniki we właściwości.</span><span class="sxs-lookup"><span data-stu-id="61037-110">The second command creates a named value and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="61037-111">Przykład 2: Tworzenie nazwanej wartości, która ma wartość tajną</span><span class="sxs-lookup"><span data-stu-id="61037-111">Example 2: Create a named value that has a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property12" -Name "Secret Property" -Value "Secret Property Value" -Secret
```

<span data-ttu-id="61037-112">To polecenie tworzy **nazwaną wartość** z zaszyfrowaną wartością.</span><span class="sxs-lookup"><span data-stu-id="61037-112">This command creates a **Named Value** that has a value that is encrypted.</span></span>

## <span data-ttu-id="61037-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="61037-113">PARAMETERS</span></span>

### <span data-ttu-id="61037-114">-Context</span><span class="sxs-lookup"><span data-stu-id="61037-114">-Context</span></span>
<span data-ttu-id="61037-115">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="61037-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="61037-116">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="61037-116">This parameter is required.</span></span>

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

### <span data-ttu-id="61037-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61037-117">-DefaultProfile</span></span>
<span data-ttu-id="61037-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="61037-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61037-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="61037-119">-Name</span></span>
<span data-ttu-id="61037-120">Nazwa wartości nazwanej.</span><span class="sxs-lookup"><span data-stu-id="61037-120">Name of the named value.</span></span>
<span data-ttu-id="61037-121">Maksymalna długość to 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="61037-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="61037-122">Może zawierać tylko litery, cyfry, kropkę, kreskę i znaki podkreślenia.</span><span class="sxs-lookup"><span data-stu-id="61037-122">It may contain only letters, digits, period, dash, and underscore characters.</span></span>
<span data-ttu-id="61037-123">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="61037-123">This parameter is required.</span></span>

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

### <span data-ttu-id="61037-124">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="61037-124">-NamedValueId</span></span>
<span data-ttu-id="61037-125">Identyfikator nowej nazwanej wartości.</span><span class="sxs-lookup"><span data-stu-id="61037-125">Identifier of new named value.</span></span>
<span data-ttu-id="61037-126">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="61037-126">This parameter is optional.</span></span>
<span data-ttu-id="61037-127">Jeśli nie określono, zostanie wygenerowana.</span><span class="sxs-lookup"><span data-stu-id="61037-127">If not specified will be generated.</span></span>

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

### <span data-ttu-id="61037-128">-Secret</span><span class="sxs-lookup"><span data-stu-id="61037-128">-Secret</span></span>
<span data-ttu-id="61037-129">Określa, czy wartość jest kluczem tajnym i czy ma być szyfrowana.</span><span class="sxs-lookup"><span data-stu-id="61037-129">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="61037-130">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="61037-130">This parameter is optional.</span></span>
<span data-ttu-id="61037-131">Wartość domyślna to false.</span><span class="sxs-lookup"><span data-stu-id="61037-131">Default Value is false.</span></span>

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

### <span data-ttu-id="61037-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="61037-132">-Tag</span></span>
<span data-ttu-id="61037-133">Znaczniki, które mają być skojarzone z nazwaną wartością.</span><span class="sxs-lookup"><span data-stu-id="61037-133">Tags to be associated with named value.</span></span>
<span data-ttu-id="61037-134">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="61037-134">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61037-135">-Value</span><span class="sxs-lookup"><span data-stu-id="61037-135">-Value</span></span>
<span data-ttu-id="61037-136">Wartość nazwanej wartości.</span><span class="sxs-lookup"><span data-stu-id="61037-136">Value of the named value.</span></span>
<span data-ttu-id="61037-137">Może zawierać wyrażenia zasad.</span><span class="sxs-lookup"><span data-stu-id="61037-137">Can contain policy expressions.</span></span>
<span data-ttu-id="61037-138">Maksymalna długość to 1000 znaków.</span><span class="sxs-lookup"><span data-stu-id="61037-138">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="61037-139">Być może nie jest on pusty lub obejmuje tylko białe znaki.</span><span class="sxs-lookup"><span data-stu-id="61037-139">It may not be empty or consist only of whitespace.</span></span>
<span data-ttu-id="61037-140">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="61037-140">This parameter is required.</span></span>

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

### <span data-ttu-id="61037-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="61037-141">-Confirm</span></span>
<span data-ttu-id="61037-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61037-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61037-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61037-143">-WhatIf</span></span>
<span data-ttu-id="61037-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61037-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61037-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="61037-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61037-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61037-146">CommonParameters</span></span>
<span data-ttu-id="61037-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61037-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61037-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61037-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61037-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61037-149">INPUTS</span></span>

### <span data-ttu-id="61037-150">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="61037-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="61037-151">System. String</span><span class="sxs-lookup"><span data-stu-id="61037-151">System.String</span></span>

### <span data-ttu-id="61037-152">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="61037-152">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="61037-153">System. String []</span><span class="sxs-lookup"><span data-stu-id="61037-153">System.String[]</span></span>

## <span data-ttu-id="61037-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="61037-154">OUTPUTS</span></span>

### <span data-ttu-id="61037-155">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="61037-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="61037-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="61037-156">NOTES</span></span>

## <span data-ttu-id="61037-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61037-157">RELATED LINKS</span></span>
