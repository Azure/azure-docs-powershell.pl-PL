---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
ms.openlocfilehash: cb50ea5735a9f63f5f35b8f1cb0648c566e6108d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718755"
---
# <span data-ttu-id="ac9dd-101">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="ac9dd-101">New-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="ac9dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ac9dd-102">SYNOPSIS</span></span>
<span data-ttu-id="ac9dd-103">Tworzy nową właściwość.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-103">Creates a new Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac9dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ac9dd-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tags <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac9dd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ac9dd-105">DESCRIPTION</span></span>
<span data-ttu-id="ac9dd-106">Polecenie cmdlet **New-AzureRmApiManagementProperty** tworzy **Właściwość** zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-106">The **New-AzureRmApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="ac9dd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ac9dd-107">EXAMPLES</span></span>

### <span data-ttu-id="ac9dd-108">Przykład 1. Tworzenie właściwości zawierającej Tagi</span><span class="sxs-lookup"><span data-stu-id="ac9dd-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="ac9dd-109">Pierwsze polecenie powoduje przypisanie dwóch wartości do zmiennej $Tags.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-109">The first command assigns two values to the $Tags variable.</span></span>

<span data-ttu-id="ac9dd-110">Drugie polecenie tworzy właściwość i przypisuje ciągi w $Tags jako znaczniki we właściwości.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="ac9dd-111">Przykład 2: Tworzenie właściwości zawierającej tajną wartość</span><span class="sxs-lookup"><span data-stu-id="ac9dd-111">Example 2: Create a property that has a secret value</span></span>
```
PS C:\>New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property -Value "Secret Property Value" -Secret
```

<span data-ttu-id="ac9dd-112">To polecenie tworzy **Właściwość** z zaszyfrowaną wartością.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="ac9dd-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ac9dd-113">PARAMETERS</span></span>

### <span data-ttu-id="ac9dd-114">-Context</span><span class="sxs-lookup"><span data-stu-id="ac9dd-114">-Context</span></span>
<span data-ttu-id="ac9dd-115">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ac9dd-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ac9dd-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ac9dd-116">-Name</span></span>
<span data-ttu-id="ac9dd-117">Określa nazwę właściwości tworzonego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-117">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="ac9dd-118">Maksymalna długość to 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-118">Maximum length is 100 characters.</span></span>
<span data-ttu-id="ac9dd-119">Nazwy zawierają tylko litery, cyfry, kropkę, kreskę i znaki podkreślenia.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-119">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="ac9dd-120">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="ac9dd-120">-PropertyId</span></span>
<span data-ttu-id="ac9dd-121">Określa identyfikator właściwości.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-121">Specifies an ID for the property.</span></span>
<span data-ttu-id="ac9dd-122">Maksymalna długość to 256 znaków.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-122">Maximum length is 256 characters.</span></span>
<span data-ttu-id="ac9dd-123">Jeśli nie określisz identyfikatora, to polecenie cmdlet wygeneruje je.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-123">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="ac9dd-124">-Secret</span><span class="sxs-lookup"><span data-stu-id="ac9dd-124">-Secret</span></span>
<span data-ttu-id="ac9dd-125">Wskazuje, że wartość właściwości jest kluczem tajnym i powinna być szyfrowana.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-125">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="ac9dd-126">-Tagi</span><span class="sxs-lookup"><span data-stu-id="ac9dd-126">-Tags</span></span>
<span data-ttu-id="ac9dd-127">Określa tablicę tagów, które są kojarzone z właściwością tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-127">Specifies an array of tags that this cmdlet associates to the property.</span></span>
<span data-ttu-id="ac9dd-128">Za pomocą znaczników można filtrować listę właściwości.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-128">You can use tags to filter the property list.</span></span>

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

### <span data-ttu-id="ac9dd-129">-Value</span><span class="sxs-lookup"><span data-stu-id="ac9dd-129">-Value</span></span>
<span data-ttu-id="ac9dd-130">Określa wartość właściwości.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-130">Specifies a value for the property.</span></span>
<span data-ttu-id="ac9dd-131">Ta wartość może zawierać wyrażenia zasad.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-131">This value can contain policy expressions.</span></span>
<span data-ttu-id="ac9dd-132">Maksymalna długość to 1000 znaków.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-132">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="ac9dd-133">Wartość nie może być pusta ani zawierać tylko odstępu.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-133">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="ac9dd-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac9dd-134">-DefaultProfile</span></span>
<span data-ttu-id="ac9dd-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac9dd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac9dd-136">CommonParameters</span></span>
<span data-ttu-id="ac9dd-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac9dd-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac9dd-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac9dd-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac9dd-139">INPUTS</span></span>

## <span data-ttu-id="ac9dd-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ac9dd-140">OUTPUTS</span></span>

### <span data-ttu-id="ac9dd-141">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="ac9dd-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="ac9dd-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ac9dd-142">NOTES</span></span>

## <span data-ttu-id="ac9dd-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ac9dd-143">RELATED LINKS</span></span>

[<span data-ttu-id="ac9dd-144">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="ac9dd-144">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)

[<span data-ttu-id="ac9dd-145">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="ac9dd-145">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


