---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
ms.openlocfilehash: 89612136023173d2f725c8c4b286a270400f8c6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718663"
---
# <span data-ttu-id="6d705-101">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="6d705-101">Set-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="6d705-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6d705-102">SYNOPSIS</span></span>
<span data-ttu-id="6d705-103">Modyfikuje Właściwość zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="6d705-103">Modifies an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d705-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6d705-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tag <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6d705-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6d705-105">DESCRIPTION</span></span>
<span data-ttu-id="6d705-106">Polecenie cmdlet **Set-AzureRmApiManagementProperty** modyfikuje Właściwość zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="6d705-106">The **Set-AzureRmApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="6d705-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6d705-107">EXAMPLES</span></span>

### <span data-ttu-id="6d705-108">Przykład 1. Zmienianie tagów właściwości</span><span class="sxs-lookup"><span data-stu-id="6d705-108">Example 1: Change the tags on a property</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="6d705-109">Pierwsze polecenie powoduje przypisanie dwóch wartości do zmiennej $Tags.</span><span class="sxs-lookup"><span data-stu-id="6d705-109">The first command assigns two values to the $Tags variable.</span></span>

<span data-ttu-id="6d705-110">Drugie polecenie modyfikuje właściwość o IDENTYFIKATORze Property11.</span><span class="sxs-lookup"><span data-stu-id="6d705-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="6d705-111">Polecenie przypisuje ciągi w $Tags jako znaczniki we właściwości.</span><span class="sxs-lookup"><span data-stu-id="6d705-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="6d705-112">Przykład 2: modyfikowanie właściwości w celu uzyskania tajnej wartości</span><span class="sxs-lookup"><span data-stu-id="6d705-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="6d705-113">To polecenie zmienia właściwość, która ma być szyfrowana.</span><span class="sxs-lookup"><span data-stu-id="6d705-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="6d705-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6d705-114">PARAMETERS</span></span>

### <span data-ttu-id="6d705-115">-Context</span><span class="sxs-lookup"><span data-stu-id="6d705-115">-Context</span></span>
<span data-ttu-id="6d705-116">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="6d705-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6d705-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d705-117">-DefaultProfile</span></span>
<span data-ttu-id="6d705-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6d705-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="6d705-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6d705-119">-Name</span></span>
<span data-ttu-id="6d705-120">Określa nazwę właściwości.</span><span class="sxs-lookup"><span data-stu-id="6d705-120">Specifies the name of the property.</span></span>
<span data-ttu-id="6d705-121">Maksymalna długość to 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="6d705-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="6d705-122">Nazwy zawierają tylko litery, cyfry, kropkę, kreskę i znaki podkreślenia.</span><span class="sxs-lookup"><span data-stu-id="6d705-122">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="6d705-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d705-123">-PassThru</span></span>
<span data-ttu-id="6d705-124">Wskazuje, że to polecenie cmdlet zwróci **PsApiManagementProperty** , które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d705-124">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="6d705-125">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="6d705-125">-PropertyId</span></span>
<span data-ttu-id="6d705-126">Określa identyfikator właściwości, która jest modyfikowana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d705-126">Specifies an ID of the property that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="6d705-127">-Secret</span><span class="sxs-lookup"><span data-stu-id="6d705-127">-Secret</span></span>
<span data-ttu-id="6d705-128">Wskazuje, że wartość właściwości jest kluczem tajnym i powinna być szyfrowana.</span><span class="sxs-lookup"><span data-stu-id="6d705-128">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d705-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="6d705-129">-Tag</span></span>
<span data-ttu-id="6d705-130">Tagi skojarzone z właściwością.</span><span class="sxs-lookup"><span data-stu-id="6d705-130">Tags associated with a property.</span></span> <span data-ttu-id="6d705-131">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="6d705-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="6d705-132">-Value</span><span class="sxs-lookup"><span data-stu-id="6d705-132">-Value</span></span>
<span data-ttu-id="6d705-133">Określa wartość właściwości.</span><span class="sxs-lookup"><span data-stu-id="6d705-133">Specifies a value for the property.</span></span>
<span data-ttu-id="6d705-134">Ta wartość może zawierać wyrażenia zasad.</span><span class="sxs-lookup"><span data-stu-id="6d705-134">This value can contain policy expressions.</span></span>
<span data-ttu-id="6d705-135">Maksymalna długość to 1000 znaków.</span><span class="sxs-lookup"><span data-stu-id="6d705-135">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="6d705-136">Wartość nie może być pusta ani zawierać tylko odstępu.</span><span class="sxs-lookup"><span data-stu-id="6d705-136">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="6d705-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d705-137">CommonParameters</span></span>
<span data-ttu-id="6d705-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d705-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d705-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d705-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d705-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d705-140">INPUTS</span></span>

### <span data-ttu-id="6d705-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6d705-141">None</span></span>
<span data-ttu-id="6d705-142">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="6d705-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6d705-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6d705-143">OUTPUTS</span></span>

### <span data-ttu-id="6d705-144">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="6d705-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="6d705-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6d705-145">NOTES</span></span>

## <span data-ttu-id="6d705-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d705-146">RELATED LINKS</span></span>

[<span data-ttu-id="6d705-147">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="6d705-147">Get-AzureRmApiManagementProperty</span></span>](./Get-AzureRmApiManagementProperty.md)

[<span data-ttu-id="6d705-148">Nowe — AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="6d705-148">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="6d705-149">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="6d705-149">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)


