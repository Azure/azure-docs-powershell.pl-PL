---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
ms.openlocfilehash: 38c937de07d4a19a6c2632356c2b9ac58b2b416a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053136"
---
# <span data-ttu-id="ef740-101">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="ef740-101">Set-AzApiManagementProperty</span></span>

## <span data-ttu-id="ef740-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ef740-102">SYNOPSIS</span></span>
<span data-ttu-id="ef740-103">Modyfikuje Właściwość zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="ef740-103">Modifies an API Management Property.</span></span>

## <span data-ttu-id="ef740-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ef740-104">SYNTAX</span></span>

```
Set-AzApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tag <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef740-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ef740-105">DESCRIPTION</span></span>
<span data-ttu-id="ef740-106">Polecenie cmdlet **Set-AzApiManagementProperty** modyfikuje Właściwość zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="ef740-106">The **Set-AzApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="ef740-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ef740-107">EXAMPLES</span></span>

### <span data-ttu-id="ef740-108">Przykład 1. Zmienianie tagów właściwości</span><span class="sxs-lookup"><span data-stu-id="ef740-108">Example 1: Change the tags on a property</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="ef740-109">Pierwsze polecenie powoduje przypisanie dwóch wartości do zmiennej $Tags.</span><span class="sxs-lookup"><span data-stu-id="ef740-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="ef740-110">Drugie polecenie modyfikuje właściwość o IDENTYFIKATORze Property11.</span><span class="sxs-lookup"><span data-stu-id="ef740-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="ef740-111">Polecenie przypisuje ciągi w $Tags jako znaczniki we właściwości.</span><span class="sxs-lookup"><span data-stu-id="ef740-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="ef740-112">Przykład 2: modyfikowanie właściwości w celu uzyskania tajnej wartości</span><span class="sxs-lookup"><span data-stu-id="ef740-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="ef740-113">To polecenie zmienia właściwość, która ma być szyfrowana.</span><span class="sxs-lookup"><span data-stu-id="ef740-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="ef740-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ef740-114">PARAMETERS</span></span>

### <span data-ttu-id="ef740-115">-Context</span><span class="sxs-lookup"><span data-stu-id="ef740-115">-Context</span></span>
<span data-ttu-id="ef740-116">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ef740-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ef740-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef740-117">-DefaultProfile</span></span>
<span data-ttu-id="ef740-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ef740-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef740-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ef740-119">-Name</span></span>
<span data-ttu-id="ef740-120">Określa nazwę właściwości.</span><span class="sxs-lookup"><span data-stu-id="ef740-120">Specifies the name of the property.</span></span>
<span data-ttu-id="ef740-121">Maksymalna długość to 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="ef740-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="ef740-122">Nazwy zawierają tylko litery, cyfry, kropkę, kreskę i znaki podkreślenia.</span><span class="sxs-lookup"><span data-stu-id="ef740-122">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="ef740-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef740-123">-PassThru</span></span>
<span data-ttu-id="ef740-124">Wskazuje, że to polecenie cmdlet zwróci **PsApiManagementProperty** , które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef740-124">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ef740-125">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="ef740-125">-PropertyId</span></span>
<span data-ttu-id="ef740-126">Określa identyfikator właściwości, która jest modyfikowana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef740-126">Specifies an ID of the property that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ef740-127">-Secret</span><span class="sxs-lookup"><span data-stu-id="ef740-127">-Secret</span></span>
<span data-ttu-id="ef740-128">Wskazuje, że wartość właściwości jest kluczem tajnym i powinna być szyfrowana.</span><span class="sxs-lookup"><span data-stu-id="ef740-128">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="ef740-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="ef740-129">-Tag</span></span>
<span data-ttu-id="ef740-130">Tagi skojarzone z właściwością.</span><span class="sxs-lookup"><span data-stu-id="ef740-130">Tags associated with a property.</span></span> <span data-ttu-id="ef740-131">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="ef740-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="ef740-132">-Value</span><span class="sxs-lookup"><span data-stu-id="ef740-132">-Value</span></span>
<span data-ttu-id="ef740-133">Określa wartość właściwości.</span><span class="sxs-lookup"><span data-stu-id="ef740-133">Specifies a value for the property.</span></span>
<span data-ttu-id="ef740-134">Ta wartość może zawierać wyrażenia zasad.</span><span class="sxs-lookup"><span data-stu-id="ef740-134">This value can contain policy expressions.</span></span>
<span data-ttu-id="ef740-135">Maksymalna długość to 1000 znaków.</span><span class="sxs-lookup"><span data-stu-id="ef740-135">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="ef740-136">Wartość nie może być pusta ani zawierać tylko odstępu.</span><span class="sxs-lookup"><span data-stu-id="ef740-136">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="ef740-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ef740-137">-Confirm</span></span>
<span data-ttu-id="ef740-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef740-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef740-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef740-139">-WhatIf</span></span>
<span data-ttu-id="ef740-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef740-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef740-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ef740-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef740-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef740-142">CommonParameters</span></span>
<span data-ttu-id="ef740-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef740-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef740-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef740-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef740-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef740-145">INPUTS</span></span>

### <span data-ttu-id="ef740-146">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ef740-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ef740-147">System. String</span><span class="sxs-lookup"><span data-stu-id="ef740-147">System.String</span></span>

### <span data-ttu-id="ef740-148">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ef740-148">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ef740-149">System. String []</span><span class="sxs-lookup"><span data-stu-id="ef740-149">System.String[]</span></span>

### <span data-ttu-id="ef740-150">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ef740-150">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ef740-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ef740-151">OUTPUTS</span></span>

### <span data-ttu-id="ef740-152">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="ef740-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="ef740-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ef740-153">NOTES</span></span>

## <span data-ttu-id="ef740-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef740-154">RELATED LINKS</span></span>

[<span data-ttu-id="ef740-155">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="ef740-155">Get-AzApiManagementProperty</span></span>](./Get-AzApiManagementProperty.md)

[<span data-ttu-id="ef740-156">Nowe — AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="ef740-156">New-AzApiManagementProperty</span></span>](./New-AzApiManagementProperty.md)

[<span data-ttu-id="ef740-157">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="ef740-157">Remove-AzApiManagementProperty</span></span>](./Remove-AzApiManagementProperty.md)


