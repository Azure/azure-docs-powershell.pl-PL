---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
ms.openlocfilehash: de61efcbabb2e5acd7d82bf7a1cec8341fe06433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542724"
---
# <span data-ttu-id="afdf5-101">Add-AzureRmVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="afdf5-101">Add-AzureRmVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="afdf5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="afdf5-102">SYNOPSIS</span></span>
<span data-ttu-id="afdf5-103">Dodaje informacje do pliku odpowiedzi instalacji nienadzorowanej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="afdf5-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afdf5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="afdf5-104">SYNTAX</span></span>

```
Add-AzureRmVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afdf5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="afdf5-105">DESCRIPTION</span></span>
<span data-ttu-id="afdf5-106">Polecenie cmdlet **Add-AzureRmVmssAdditionalUnattendContent** umożliwia dodanie informacji do pliku odpowiedzi instalacji nienadzorowanej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="afdf5-106">The **Add-AzureRmVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="afdf5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="afdf5-107">EXAMPLES</span></span>

### <span data-ttu-id="afdf5-108">Przykład 1. Dodawanie informacji do pliku odpowiedzi instalacji nienadzorowanej systemu Windows</span><span class="sxs-lookup"><span data-stu-id="afdf5-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzureRmVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="afdf5-109">To polecenie umożliwia dodanie informacji do pliku odpowiedzi instalacji nienadzorowanej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="afdf5-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="afdf5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="afdf5-110">PARAMETERS</span></span>

### <span data-ttu-id="afdf5-111">-Składnikname</span><span class="sxs-lookup"><span data-stu-id="afdf5-111">-ComponentName</span></span>
<span data-ttu-id="afdf5-112">Określa nazwę składnika do skonfigurowania przy użyciu dodanej zawartości.</span><span class="sxs-lookup"><span data-stu-id="afdf5-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="afdf5-113">Jedyną dozwoloną wartością jest Microsoft-Windows-Shell-Setup.</span><span class="sxs-lookup"><span data-stu-id="afdf5-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

```yaml
Type: ComponentNames
Parameter Sets: (All)
Aliases: 
Accepted values: MicrosoftWindowsShellSetup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afdf5-114">-Content (zawartość)</span><span class="sxs-lookup"><span data-stu-id="afdf5-114">-Content</span></span>
<span data-ttu-id="afdf5-115">Określa zawartość w formacie XML, która jest dodawana do pliku unattend.xml określonej ścieżki i składnika.</span><span class="sxs-lookup"><span data-stu-id="afdf5-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afdf5-116">-Passname</span><span class="sxs-lookup"><span data-stu-id="afdf5-116">-PassName</span></span>
<span data-ttu-id="afdf5-117">Określa nazwę przebiegu, do którego odnosi się zawartość.</span><span class="sxs-lookup"><span data-stu-id="afdf5-117">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="afdf5-118">Jedyną dozwoloną wartością jest oobeSystem.</span><span class="sxs-lookup"><span data-stu-id="afdf5-118">The only allowable value is oobeSystem.</span></span>

```yaml
Type: PassNames
Parameter Sets: (All)
Aliases: 
Accepted values: OobeSystem

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afdf5-119">-SettingName</span><span class="sxs-lookup"><span data-stu-id="afdf5-119">-SettingName</span></span>
<span data-ttu-id="afdf5-120">Określa nazwę ustawienia, którego dotyczy zawartość.</span><span class="sxs-lookup"><span data-stu-id="afdf5-120">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="afdf5-121">Dopuszczalne wartości tego parametru to::</span><span class="sxs-lookup"><span data-stu-id="afdf5-121">The acceptable values for this parameter are::</span></span>

- <span data-ttu-id="afdf5-122">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="afdf5-122">FirstLogonCommands</span></span>
- <span data-ttu-id="afdf5-123">Autologowanie</span><span class="sxs-lookup"><span data-stu-id="afdf5-123">AutoLogon</span></span>

```yaml
Type: SettingNames
Parameter Sets: (All)
Aliases: 
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afdf5-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="afdf5-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="afdf5-125">Określ obiekt **zestawu skali** maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="afdf5-125">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="afdf5-126">Aby utworzyć obiekt, możesz użyć polecenia cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="afdf5-126">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="afdf5-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="afdf5-127">-Confirm</span></span>
<span data-ttu-id="afdf5-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afdf5-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afdf5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afdf5-129">-WhatIf</span></span>
<span data-ttu-id="afdf5-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afdf5-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="afdf5-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="afdf5-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afdf5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afdf5-132">CommonParameters</span></span>
<span data-ttu-id="afdf5-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afdf5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afdf5-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afdf5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afdf5-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="afdf5-135">INPUTS</span></span>

### <span data-ttu-id="afdf5-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="afdf5-136">None</span></span>
<span data-ttu-id="afdf5-137">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="afdf5-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="afdf5-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="afdf5-138">OUTPUTS</span></span>

## <span data-ttu-id="afdf5-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="afdf5-139">NOTES</span></span>

## <span data-ttu-id="afdf5-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="afdf5-140">RELATED LINKS</span></span>

[<span data-ttu-id="afdf5-141">Nowe — AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="afdf5-141">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
