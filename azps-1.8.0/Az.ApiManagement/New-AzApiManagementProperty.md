---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProperty.md
ms.openlocfilehash: d54665b767d10edde564450ecfcdd467b784dd8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869496"
---
# <span data-ttu-id="45b16-101">New-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="45b16-101">New-AzApiManagementProperty</span></span>

## <span data-ttu-id="45b16-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45b16-102">SYNOPSIS</span></span>
<span data-ttu-id="45b16-103">Tworzy nową właściwość.</span><span class="sxs-lookup"><span data-stu-id="45b16-103">Creates a new Property.</span></span>

## <span data-ttu-id="45b16-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45b16-104">SYNTAX</span></span>

```
New-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45b16-105">Opis</span><span class="sxs-lookup"><span data-stu-id="45b16-105">DESCRIPTION</span></span>
<span data-ttu-id="45b16-106">Polecenie cmdlet **New-AzApiManagementProperty** tworzy **Właściwość** zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="45b16-106">The **New-AzApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="45b16-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45b16-107">EXAMPLES</span></span>

### <span data-ttu-id="45b16-108">Przykład 1. Tworzenie właściwości zawierającej Tagi</span><span class="sxs-lookup"><span data-stu-id="45b16-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="45b16-109">Pierwsze polecenie powoduje przypisanie dwóch wartości do zmiennej $Tags.</span><span class="sxs-lookup"><span data-stu-id="45b16-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="45b16-110">Drugie polecenie tworzy właściwość i przypisuje ciągi w $Tags jako znaczniki we właściwości.</span><span class="sxs-lookup"><span data-stu-id="45b16-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="45b16-111">Przykład 2: Tworzenie właściwości zawierającej tajną wartość</span><span class="sxs-lookup"><span data-stu-id="45b16-111">Example 2: Create a property that has a secret value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property -Value "Secret Property Value" -Secret
```

<span data-ttu-id="45b16-112">To polecenie tworzy **Właściwość** z zaszyfrowaną wartością.</span><span class="sxs-lookup"><span data-stu-id="45b16-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="45b16-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45b16-113">PARAMETERS</span></span>

### <span data-ttu-id="45b16-114">-Context</span><span class="sxs-lookup"><span data-stu-id="45b16-114">-Context</span></span>
<span data-ttu-id="45b16-115">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="45b16-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="45b16-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45b16-116">-DefaultProfile</span></span>
<span data-ttu-id="45b16-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="45b16-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45b16-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="45b16-118">-Name</span></span>
<span data-ttu-id="45b16-119">Określa nazwę właściwości tworzonego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45b16-119">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="45b16-120">Maksymalna długość to 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="45b16-120">Maximum length is 100 characters.</span></span>
<span data-ttu-id="45b16-121">Nazwy zawierają tylko litery, cyfry, kropkę, kreskę i znaki podkreślenia.</span><span class="sxs-lookup"><span data-stu-id="45b16-121">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="45b16-122">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="45b16-122">-PropertyId</span></span>
<span data-ttu-id="45b16-123">Określa identyfikator właściwości.</span><span class="sxs-lookup"><span data-stu-id="45b16-123">Specifies an ID for the property.</span></span>
<span data-ttu-id="45b16-124">Maksymalna długość to 256 znaków.</span><span class="sxs-lookup"><span data-stu-id="45b16-124">Maximum length is 256 characters.</span></span>
<span data-ttu-id="45b16-125">Jeśli nie określisz identyfikatora, to polecenie cmdlet wygeneruje je.</span><span class="sxs-lookup"><span data-stu-id="45b16-125">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="45b16-126">-Secret</span><span class="sxs-lookup"><span data-stu-id="45b16-126">-Secret</span></span>
<span data-ttu-id="45b16-127">Wskazuje, że wartość właściwości jest kluczem tajnym i powinna być szyfrowana.</span><span class="sxs-lookup"><span data-stu-id="45b16-127">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="45b16-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="45b16-128">-Tag</span></span>
<span data-ttu-id="45b16-129">Tagi, które mają być skojarzone z właściwością.</span><span class="sxs-lookup"><span data-stu-id="45b16-129">Tags to be associated with Property.</span></span> <span data-ttu-id="45b16-130">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="45b16-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="45b16-131">-Value</span><span class="sxs-lookup"><span data-stu-id="45b16-131">-Value</span></span>
<span data-ttu-id="45b16-132">Określa wartość właściwości.</span><span class="sxs-lookup"><span data-stu-id="45b16-132">Specifies a value for the property.</span></span>
<span data-ttu-id="45b16-133">Ta wartość może zawierać wyrażenia zasad.</span><span class="sxs-lookup"><span data-stu-id="45b16-133">This value can contain policy expressions.</span></span>
<span data-ttu-id="45b16-134">Maksymalna długość to 1000 znaków.</span><span class="sxs-lookup"><span data-stu-id="45b16-134">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="45b16-135">Wartość nie może być pusta ani zawierać tylko odstępu.</span><span class="sxs-lookup"><span data-stu-id="45b16-135">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="45b16-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45b16-136">CommonParameters</span></span>
<span data-ttu-id="45b16-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45b16-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45b16-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45b16-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45b16-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45b16-139">INPUTS</span></span>

### <span data-ttu-id="45b16-140">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="45b16-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="45b16-141">System. String</span><span class="sxs-lookup"><span data-stu-id="45b16-141">System.String</span></span>

### <span data-ttu-id="45b16-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="45b16-142">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="45b16-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="45b16-143">System.String[]</span></span>

## <span data-ttu-id="45b16-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45b16-144">OUTPUTS</span></span>

### <span data-ttu-id="45b16-145">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="45b16-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="45b16-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45b16-146">NOTES</span></span>

## <span data-ttu-id="45b16-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45b16-147">RELATED LINKS</span></span>

[<span data-ttu-id="45b16-148">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="45b16-148">Remove-AzApiManagementProperty</span></span>](./Remove-AzApiManagementProperty.md)

[<span data-ttu-id="45b16-149">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="45b16-149">Set-AzApiManagementProperty</span></span>](./Set-AzApiManagementProperty.md)


