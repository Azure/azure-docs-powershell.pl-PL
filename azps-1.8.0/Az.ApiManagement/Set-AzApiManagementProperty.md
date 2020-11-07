---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
ms.openlocfilehash: b12a904be944b4a6338ad0bf34a4c906382cb910
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869323"
---
# <span data-ttu-id="ec5fa-101">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="ec5fa-101">Set-AzApiManagementProperty</span></span>

## <span data-ttu-id="ec5fa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ec5fa-102">SYNOPSIS</span></span>
<span data-ttu-id="ec5fa-103">Modyfikuje Właściwość zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="ec5fa-103">Modifies an API Management Property.</span></span>

## <span data-ttu-id="ec5fa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ec5fa-104">SYNTAX</span></span>

```
Set-AzApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tag <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec5fa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ec5fa-105">DESCRIPTION</span></span>
<span data-ttu-id="ec5fa-106">Polecenie cmdlet **Set-AzApiManagementProperty** modyfikuje Właściwość zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="ec5fa-106">The **Set-AzApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="ec5fa-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ec5fa-107">EXAMPLES</span></span>

### <span data-ttu-id="ec5fa-108">Przykład 1. Zmienianie tagów właściwości</span><span class="sxs-lookup"><span data-stu-id="ec5fa-108">Example 1: Change the tags on a property</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="ec5fa-109">Pierwsze polecenie powoduje przypisanie dwóch wartości do zmiennej $Tags.</span><span class="sxs-lookup"><span data-stu-id="ec5fa-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="ec5fa-110">Drugie polecenie modyfikuje właściwość o IDENTYFIKATORze Property11.</span><span class="sxs-lookup"><span data-stu-id="ec5fa-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="ec5fa-111">Polecenie przypisuje ciągi w $Tags jako znaczniki we właściwości.</span><span class="sxs-lookup"><span data-stu-id="ec5fa-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="ec5fa-112">Przykład 2: modyfikowanie właściwości w celu uzyskania tajnej wartości</span><span class="sxs-lookup"><span data-stu-id="ec5fa-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="ec5fa-113">To polecenie zmienia właściwość, która ma być szyfrowana.</span><span class="sxs-lookup"><span data-stu-id="ec5fa-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="ec5fa-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ec5fa-114">PARAMETERS</span></span>

### <span data-ttu-id="ec5fa-115">-Context</span><span class="sxs-lookup"><span data-stu-id="ec5fa-115">-Context</span></span>
<span data-ttu-id="ec5fa-116">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ec5fa-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ec5fa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec5fa-117">-DefaultProfile</span></span>
<span data-ttu-id="ec5fa-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ec5fa-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec5fa-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ec5fa-119">-Name</span></span>
<span data-ttu-id="ec5fa-120">Określa nazwę właściwości.</span><span class="sxs-lookup"><span data-stu-id="ec5fa-120">Specifies the name of the property.</span></span>
<span data-ttu-id="ec5fa-121">Maksymalna długość to 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="ec5fa-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="ec5fa-122">Nazwy zawierają tylko litery, cyfry, kropkę, kreskę i znaki podkreślenia.</span><span class="sxs-lookup"><span data-stu-id="ec5fa-122">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="ec5fa-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec5fa-123">-PassThru</span></span>
<span data-ttu-id="ec5fa-124">Wskazuje, że to polecenie cmdlet zwróci **PsApiManagementProperty** , które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec5fa-124">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ec5fa-125">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="ec5fa-125">-PropertyId</span></span>
<span data-ttu-id="ec5fa-126">Określa identyfikator właściwości, która jest modyfikowana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec5fa-126">Specifies an ID of the property that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ec5fa-127">-Secret</span><span class="sxs-lookup"><span data-stu-id="ec5fa-127">-Secret</span></span>
<span data-ttu-id="ec5fa-128">Wskazuje, że wartość właściwości jest kluczem tajnym i powinna być szyfrowana.</span><span class="sxs-lookup"><span data-stu-id="ec5fa-128">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="ec5fa-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="ec5fa-129">-Tag</span></span>
<span data-ttu-id="ec5fa-130">Tagi skojarzone z właściwością.</span><span class="sxs-lookup"><span data-stu-id="ec5fa-130">Tags associated with a property.</span></span> <span data-ttu-id="ec5fa-131">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="ec5fa-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="ec5fa-132">-Value</span><span class="sxs-lookup"><span data-stu-id="ec5fa-132">-Value</span></span>
<span data-ttu-id="ec5fa-133">Określa wartość właściwości.</span><span class="sxs-lookup"><span data-stu-id="ec5fa-133">Specifies a value for the property.</span></span>
<span data-ttu-id="ec5fa-134">Ta wartość może zawierać wyrażenia zasad.</span><span class="sxs-lookup"><span data-stu-id="ec5fa-134">This value can contain policy expressions.</span></span>
<span data-ttu-id="ec5fa-135">Maksymalna długość to 1000 znaków.</span><span class="sxs-lookup"><span data-stu-id="ec5fa-135">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="ec5fa-136">Wartość nie może być pusta ani zawierać tylko odstępu.</span><span class="sxs-lookup"><span data-stu-id="ec5fa-136">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="ec5fa-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec5fa-137">CommonParameters</span></span>
<span data-ttu-id="ec5fa-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec5fa-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec5fa-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec5fa-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec5fa-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec5fa-140">INPUTS</span></span>

### <span data-ttu-id="ec5fa-141">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ec5fa-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ec5fa-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ec5fa-142">System.String</span></span>

### <span data-ttu-id="ec5fa-143">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ec5fa-143">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ec5fa-144">System. String []</span><span class="sxs-lookup"><span data-stu-id="ec5fa-144">System.String[]</span></span>

### <span data-ttu-id="ec5fa-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ec5fa-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ec5fa-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ec5fa-146">OUTPUTS</span></span>

### <span data-ttu-id="ec5fa-147">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="ec5fa-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="ec5fa-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ec5fa-148">NOTES</span></span>

## <span data-ttu-id="ec5fa-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec5fa-149">RELATED LINKS</span></span>

[<span data-ttu-id="ec5fa-150">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="ec5fa-150">Get-AzApiManagementProperty</span></span>](./Get-AzApiManagementProperty.md)

[<span data-ttu-id="ec5fa-151">Nowe — AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="ec5fa-151">New-AzApiManagementProperty</span></span>](./New-AzApiManagementProperty.md)

[<span data-ttu-id="ec5fa-152">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="ec5fa-152">Remove-AzApiManagementProperty</span></span>](./Remove-AzApiManagementProperty.md)


