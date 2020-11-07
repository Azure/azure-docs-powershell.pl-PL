---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
ms.openlocfilehash: 38f510602259ca799c6df947b9d74984dff178ba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893886"
---
# <span data-ttu-id="bc72a-101">Add-AzVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="bc72a-101">Add-AzVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="bc72a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bc72a-102">SYNOPSIS</span></span>
<span data-ttu-id="bc72a-103">Dodaje informacje do pliku odpowiedzi instalacji nienadzorowanej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="bc72a-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="bc72a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bc72a-104">SYNTAX</span></span>

```
Add-AzVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc72a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bc72a-105">DESCRIPTION</span></span>
<span data-ttu-id="bc72a-106">Polecenie cmdlet **Add-AzVmssAdditionalUnattendContent** umożliwia dodanie informacji do pliku odpowiedzi instalacji nienadzorowanej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="bc72a-106">The **Add-AzVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="bc72a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bc72a-107">EXAMPLES</span></span>

### <span data-ttu-id="bc72a-108">Przykład 1. Dodawanie informacji do pliku odpowiedzi instalacji nienadzorowanej systemu Windows</span><span class="sxs-lookup"><span data-stu-id="bc72a-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="bc72a-109">To polecenie umożliwia dodanie informacji do pliku odpowiedzi instalacji nienadzorowanej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="bc72a-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="bc72a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bc72a-110">PARAMETERS</span></span>

### <span data-ttu-id="bc72a-111">-Składnikname</span><span class="sxs-lookup"><span data-stu-id="bc72a-111">-ComponentName</span></span>
<span data-ttu-id="bc72a-112">Określa nazwę składnika do skonfigurowania przy użyciu dodanej zawartości.</span><span class="sxs-lookup"><span data-stu-id="bc72a-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="bc72a-113">Jedyną dozwoloną wartością jest Microsoft-Windows-Shell-Setup.</span><span class="sxs-lookup"><span data-stu-id="bc72a-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

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

### <span data-ttu-id="bc72a-114">-Content (zawartość)</span><span class="sxs-lookup"><span data-stu-id="bc72a-114">-Content</span></span>
<span data-ttu-id="bc72a-115">Określa zawartość w formacie XML, która jest dodawana do pliku unattend.xml określonej ścieżki i składnika.</span><span class="sxs-lookup"><span data-stu-id="bc72a-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

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

### <span data-ttu-id="bc72a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc72a-116">-DefaultProfile</span></span>
<span data-ttu-id="bc72a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc72a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc72a-118">-Passname</span><span class="sxs-lookup"><span data-stu-id="bc72a-118">-PassName</span></span>
<span data-ttu-id="bc72a-119">Określa nazwę przebiegu, do którego odnosi się zawartość.</span><span class="sxs-lookup"><span data-stu-id="bc72a-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="bc72a-120">Jedyną dozwoloną wartością jest oobeSystem.</span><span class="sxs-lookup"><span data-stu-id="bc72a-120">The only allowable value is oobeSystem.</span></span>

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

### <span data-ttu-id="bc72a-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="bc72a-121">-SettingName</span></span>
<span data-ttu-id="bc72a-122">Określa nazwę ustawienia, którego dotyczy zawartość.</span><span class="sxs-lookup"><span data-stu-id="bc72a-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="bc72a-123">Dopuszczalne wartości tego parametru to::</span><span class="sxs-lookup"><span data-stu-id="bc72a-123">The acceptable values for this parameter are::</span></span>

- <span data-ttu-id="bc72a-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="bc72a-124">FirstLogonCommands</span></span>
- <span data-ttu-id="bc72a-125">Autologowanie</span><span class="sxs-lookup"><span data-stu-id="bc72a-125">AutoLogon</span></span>

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

### <span data-ttu-id="bc72a-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bc72a-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="bc72a-127">Określ obiekt **zestawu skali** maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bc72a-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="bc72a-128">Aby utworzyć obiekt, możesz użyć polecenia cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="bc72a-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc72a-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bc72a-129">-Confirm</span></span>
<span data-ttu-id="bc72a-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc72a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc72a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc72a-131">-WhatIf</span></span>
<span data-ttu-id="bc72a-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc72a-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc72a-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bc72a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc72a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc72a-134">CommonParameters</span></span>
<span data-ttu-id="bc72a-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc72a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc72a-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc72a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc72a-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc72a-137">INPUTS</span></span>

### <span data-ttu-id="bc72a-138">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bc72a-138">VirtualMachineScaleSet</span></span>
<span data-ttu-id="bc72a-139">Parametr "VirtualMachineScaleSet" akceptuje wartość typu "VirtualMachineScaleSet" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="bc72a-139">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="bc72a-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bc72a-140">OUTPUTS</span></span>

### <span data-ttu-id="bc72a-141">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bc72a-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="bc72a-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bc72a-142">NOTES</span></span>

## <span data-ttu-id="bc72a-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc72a-143">RELATED LINKS</span></span>

[<span data-ttu-id="bc72a-144">Nowe — AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="bc72a-144">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
