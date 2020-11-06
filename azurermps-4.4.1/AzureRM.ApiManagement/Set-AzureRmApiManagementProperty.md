---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
ms.openlocfilehash: 5273161b18f49e2cfd8f772987d8f0d9ce90bc69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525745"
---
# <span data-ttu-id="385b6-101">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="385b6-101">Set-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="385b6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="385b6-102">SYNOPSIS</span></span>
<span data-ttu-id="385b6-103">Modyfikuje Właściwość zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="385b6-103">Modifies an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="385b6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="385b6-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tags <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="385b6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="385b6-105">DESCRIPTION</span></span>
<span data-ttu-id="385b6-106">Polecenie cmdlet **Set-AzureRmApiManagementProperty** modyfikuje Właściwość zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="385b6-106">The **Set-AzureRmApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="385b6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="385b6-107">EXAMPLES</span></span>

### <span data-ttu-id="385b6-108">Przykład 1. Zmienianie tagów właściwości</span><span class="sxs-lookup"><span data-stu-id="385b6-108">Example 1: Change the tags on a property</span></span>
```
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="385b6-109">Pierwsze polecenie powoduje przypisanie dwóch wartości do zmiennej $Tags.</span><span class="sxs-lookup"><span data-stu-id="385b6-109">The first command assigns two values to the $Tags variable.</span></span>

<span data-ttu-id="385b6-110">Drugie polecenie modyfikuje właściwość o IDENTYFIKATORze Property11.</span><span class="sxs-lookup"><span data-stu-id="385b6-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="385b6-111">Polecenie przypisuje ciągi w $Tags jako znaczniki we właściwości.</span><span class="sxs-lookup"><span data-stu-id="385b6-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="385b6-112">Przykład 2: modyfikowanie właściwości w celu uzyskania tajnej wartości</span><span class="sxs-lookup"><span data-stu-id="385b6-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>Set-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="385b6-113">To polecenie zmienia właściwość, która ma być szyfrowana.</span><span class="sxs-lookup"><span data-stu-id="385b6-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="385b6-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="385b6-114">PARAMETERS</span></span>

### <span data-ttu-id="385b6-115">-Context</span><span class="sxs-lookup"><span data-stu-id="385b6-115">-Context</span></span>
<span data-ttu-id="385b6-116">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="385b6-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="385b6-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="385b6-117">-Name</span></span>
<span data-ttu-id="385b6-118">Określa nazwę właściwości.</span><span class="sxs-lookup"><span data-stu-id="385b6-118">Specifies the name of the property.</span></span>
<span data-ttu-id="385b6-119">Maksymalna długość to 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="385b6-119">Maximum length is 100 characters.</span></span>
<span data-ttu-id="385b6-120">Nazwy zawierają tylko litery, cyfry, kropkę, kreskę i znaki podkreślenia.</span><span class="sxs-lookup"><span data-stu-id="385b6-120">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="385b6-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="385b6-121">-PassThru</span></span>
<span data-ttu-id="385b6-122">Wskazuje, że to polecenie cmdlet zwróci **PsApiManagementProperty** , które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="385b6-122">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="385b6-123">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="385b6-123">-PropertyId</span></span>
<span data-ttu-id="385b6-124">Określa identyfikator właściwości, która jest modyfikowana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="385b6-124">Specifies an ID of the property that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="385b6-125">-Secret</span><span class="sxs-lookup"><span data-stu-id="385b6-125">-Secret</span></span>
<span data-ttu-id="385b6-126">Wskazuje, że wartość właściwości jest kluczem tajnym i powinna być szyfrowana.</span><span class="sxs-lookup"><span data-stu-id="385b6-126">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="385b6-127">-Tagi</span><span class="sxs-lookup"><span data-stu-id="385b6-127">-Tags</span></span>
<span data-ttu-id="385b6-128">Określa tablicę tagów, które są kojarzone z właściwością tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="385b6-128">Specifies an array of tags that this cmdlet associates to the property.</span></span>
<span data-ttu-id="385b6-129">Za pomocą znaczników można filtrować listę właściwości.</span><span class="sxs-lookup"><span data-stu-id="385b6-129">You can use tags to filter the property list.</span></span>

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

### <span data-ttu-id="385b6-130">-Value</span><span class="sxs-lookup"><span data-stu-id="385b6-130">-Value</span></span>
<span data-ttu-id="385b6-131">Określa wartość właściwości.</span><span class="sxs-lookup"><span data-stu-id="385b6-131">Specifies a value for the property.</span></span>
<span data-ttu-id="385b6-132">Ta wartość może zawierać wyrażenia zasad.</span><span class="sxs-lookup"><span data-stu-id="385b6-132">This value can contain policy expressions.</span></span>
<span data-ttu-id="385b6-133">Maksymalna długość to 1000 znaków.</span><span class="sxs-lookup"><span data-stu-id="385b6-133">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="385b6-134">Wartość nie może być pusta ani zawierać tylko odstępu.</span><span class="sxs-lookup"><span data-stu-id="385b6-134">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="385b6-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="385b6-135">-DefaultProfile</span></span>
<span data-ttu-id="385b6-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="385b6-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="385b6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="385b6-137">CommonParameters</span></span>
<span data-ttu-id="385b6-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="385b6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="385b6-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="385b6-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="385b6-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="385b6-140">INPUTS</span></span>

## <span data-ttu-id="385b6-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="385b6-141">OUTPUTS</span></span>

### <span data-ttu-id="385b6-142">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="385b6-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="385b6-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="385b6-143">NOTES</span></span>

## <span data-ttu-id="385b6-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="385b6-144">RELATED LINKS</span></span>

[<span data-ttu-id="385b6-145">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="385b6-145">Get-AzureRmApiManagementProperty</span></span>](./Get-AzureRmApiManagementProperty.md)

[<span data-ttu-id="385b6-146">Nowe — AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="385b6-146">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="385b6-147">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="385b6-147">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)


