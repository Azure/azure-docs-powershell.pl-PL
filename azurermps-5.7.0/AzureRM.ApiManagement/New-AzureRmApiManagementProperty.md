---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
ms.openlocfilehash: 55ef0d4ef714c1d434915def403f5560244a3697
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719601"
---
# <span data-ttu-id="abe30-101">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="abe30-101">New-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="abe30-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="abe30-102">SYNOPSIS</span></span>
<span data-ttu-id="abe30-103">Tworzy nową właściwość.</span><span class="sxs-lookup"><span data-stu-id="abe30-103">Creates a new Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abe30-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="abe30-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abe30-105">Opis</span><span class="sxs-lookup"><span data-stu-id="abe30-105">DESCRIPTION</span></span>
<span data-ttu-id="abe30-106">Polecenie cmdlet **New-AzureRmApiManagementProperty** tworzy **Właściwość** zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="abe30-106">The **New-AzureRmApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="abe30-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="abe30-107">EXAMPLES</span></span>

### <span data-ttu-id="abe30-108">Przykład 1. Tworzenie właściwości zawierającej Tagi</span><span class="sxs-lookup"><span data-stu-id="abe30-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="abe30-109">Pierwsze polecenie powoduje przypisanie dwóch wartości do zmiennej $Tags.</span><span class="sxs-lookup"><span data-stu-id="abe30-109">The first command assigns two values to the $Tags variable.</span></span>

<span data-ttu-id="abe30-110">Drugie polecenie tworzy właściwość i przypisuje ciągi w $Tags jako znaczniki we właściwości.</span><span class="sxs-lookup"><span data-stu-id="abe30-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="abe30-111">Przykład 2: Tworzenie właściwości zawierającej tajną wartość</span><span class="sxs-lookup"><span data-stu-id="abe30-111">Example 2: Create a property that has a secret value</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property -Value "Secret Property Value" -Secret
```

<span data-ttu-id="abe30-112">To polecenie tworzy **Właściwość** z zaszyfrowaną wartością.</span><span class="sxs-lookup"><span data-stu-id="abe30-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="abe30-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="abe30-113">PARAMETERS</span></span>

### <span data-ttu-id="abe30-114">-Context</span><span class="sxs-lookup"><span data-stu-id="abe30-114">-Context</span></span>
<span data-ttu-id="abe30-115">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="abe30-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="abe30-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abe30-116">-DefaultProfile</span></span>
<span data-ttu-id="abe30-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="abe30-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="abe30-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="abe30-118">-Name</span></span>
<span data-ttu-id="abe30-119">Określa nazwę właściwości tworzonego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abe30-119">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="abe30-120">Maksymalna długość to 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="abe30-120">Maximum length is 100 characters.</span></span>
<span data-ttu-id="abe30-121">Nazwy zawierają tylko litery, cyfry, kropkę, kreskę i znaki podkreślenia.</span><span class="sxs-lookup"><span data-stu-id="abe30-121">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abe30-122">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="abe30-122">-PropertyId</span></span>
<span data-ttu-id="abe30-123">Określa identyfikator właściwości.</span><span class="sxs-lookup"><span data-stu-id="abe30-123">Specifies an ID for the property.</span></span>
<span data-ttu-id="abe30-124">Maksymalna długość to 256 znaków.</span><span class="sxs-lookup"><span data-stu-id="abe30-124">Maximum length is 256 characters.</span></span>
<span data-ttu-id="abe30-125">Jeśli nie określisz identyfikatora, to polecenie cmdlet wygeneruje je.</span><span class="sxs-lookup"><span data-stu-id="abe30-125">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="abe30-126">-Secret</span><span class="sxs-lookup"><span data-stu-id="abe30-126">-Secret</span></span>
<span data-ttu-id="abe30-127">Wskazuje, że wartość właściwości jest kluczem tajnym i powinna być szyfrowana.</span><span class="sxs-lookup"><span data-stu-id="abe30-127">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="abe30-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="abe30-128">-Tag</span></span>
<span data-ttu-id="abe30-129">Tagi, które mają być skojarzone z właściwością.</span><span class="sxs-lookup"><span data-stu-id="abe30-129">Tags to be associated with Property.</span></span> <span data-ttu-id="abe30-130">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="abe30-130">This parameter is optional.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abe30-131">-Value</span><span class="sxs-lookup"><span data-stu-id="abe30-131">-Value</span></span>
<span data-ttu-id="abe30-132">Określa wartość właściwości.</span><span class="sxs-lookup"><span data-stu-id="abe30-132">Specifies a value for the property.</span></span>
<span data-ttu-id="abe30-133">Ta wartość może zawierać wyrażenia zasad.</span><span class="sxs-lookup"><span data-stu-id="abe30-133">This value can contain policy expressions.</span></span>
<span data-ttu-id="abe30-134">Maksymalna długość to 1000 znaków.</span><span class="sxs-lookup"><span data-stu-id="abe30-134">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="abe30-135">Wartość nie może być pusta ani zawierać tylko odstępu.</span><span class="sxs-lookup"><span data-stu-id="abe30-135">The value may not be empty or consist only of whitespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abe30-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abe30-136">CommonParameters</span></span>
<span data-ttu-id="abe30-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abe30-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abe30-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abe30-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abe30-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="abe30-139">INPUTS</span></span>

### <span data-ttu-id="abe30-140">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="abe30-140">None</span></span>
<span data-ttu-id="abe30-141">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="abe30-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="abe30-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="abe30-142">OUTPUTS</span></span>

### <span data-ttu-id="abe30-143">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="abe30-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="abe30-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="abe30-144">NOTES</span></span>

## <span data-ttu-id="abe30-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="abe30-145">RELATED LINKS</span></span>

[<span data-ttu-id="abe30-146">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="abe30-146">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)

[<span data-ttu-id="abe30-147">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="abe30-147">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)

