---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssadditionalunattendcontent
schema: 2.0.0
ms.openlocfilehash: c0ceb74c6880508f04fb0832c48d0752507f5a5b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898097"
---
# <span data-ttu-id="cf0d2-101">Add-AzureRmVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="cf0d2-101">Add-AzureRmVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="cf0d2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cf0d2-102">SYNOPSIS</span></span>
<span data-ttu-id="cf0d2-103">Dodaje informacje do pliku odpowiedzi instalacji nienadzorowanej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="cf0d2-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf0d2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cf0d2-104">SYNTAX</span></span>

```
Add-AzureRmVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf0d2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cf0d2-105">DESCRIPTION</span></span>
<span data-ttu-id="cf0d2-106">Polecenie cmdlet **Add-AzureRmVmssAdditionalUnattendContent** umożliwia dodanie informacji do pliku odpowiedzi instalacji nienadzorowanej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="cf0d2-106">The **Add-AzureRmVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="cf0d2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cf0d2-107">EXAMPLES</span></span>

### <span data-ttu-id="cf0d2-108">Przykład 1. Dodawanie informacji do pliku odpowiedzi instalacji nienadzorowanej systemu Windows</span><span class="sxs-lookup"><span data-stu-id="cf0d2-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzureRmVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="cf0d2-109">To polecenie umożliwia dodanie informacji do pliku odpowiedzi instalacji nienadzorowanej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="cf0d2-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="cf0d2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cf0d2-110">PARAMETERS</span></span>

### <span data-ttu-id="cf0d2-111">-Składnikname</span><span class="sxs-lookup"><span data-stu-id="cf0d2-111">-ComponentName</span></span>
<span data-ttu-id="cf0d2-112">Określa nazwę składnika do skonfigurowania przy użyciu dodanej zawartości.</span><span class="sxs-lookup"><span data-stu-id="cf0d2-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="cf0d2-113">Jedyną dozwoloną wartością jest Microsoft-Windows-Shell-Setup.</span><span class="sxs-lookup"><span data-stu-id="cf0d2-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

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

### <span data-ttu-id="cf0d2-114">-Content (zawartość)</span><span class="sxs-lookup"><span data-stu-id="cf0d2-114">-Content</span></span>
<span data-ttu-id="cf0d2-115">Określa zawartość w formacie XML, która jest dodawana do pliku unattend.xml określonej ścieżki i składnika.</span><span class="sxs-lookup"><span data-stu-id="cf0d2-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

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

### <span data-ttu-id="cf0d2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf0d2-116">-DefaultProfile</span></span>
<span data-ttu-id="cf0d2-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cf0d2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf0d2-118">-Passname</span><span class="sxs-lookup"><span data-stu-id="cf0d2-118">-PassName</span></span>
<span data-ttu-id="cf0d2-119">Określa nazwę przebiegu, do którego odnosi się zawartość.</span><span class="sxs-lookup"><span data-stu-id="cf0d2-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="cf0d2-120">Jedyną dozwoloną wartością jest oobeSystem.</span><span class="sxs-lookup"><span data-stu-id="cf0d2-120">The only allowable value is oobeSystem.</span></span>

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

### <span data-ttu-id="cf0d2-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="cf0d2-121">-SettingName</span></span>
<span data-ttu-id="cf0d2-122">Określa nazwę ustawienia, którego dotyczy zawartość.</span><span class="sxs-lookup"><span data-stu-id="cf0d2-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="cf0d2-123">Dopuszczalne wartości tego parametru to::</span><span class="sxs-lookup"><span data-stu-id="cf0d2-123">The acceptable values for this parameter are::</span></span>

- <span data-ttu-id="cf0d2-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="cf0d2-124">FirstLogonCommands</span></span>
- <span data-ttu-id="cf0d2-125">Autologowanie</span><span class="sxs-lookup"><span data-stu-id="cf0d2-125">AutoLogon</span></span>

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

### <span data-ttu-id="cf0d2-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cf0d2-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="cf0d2-127">Określ obiekt **zestawu skali** maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cf0d2-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="cf0d2-128">Aby utworzyć obiekt, możesz użyć polecenia cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="cf0d2-128">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="cf0d2-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cf0d2-129">-Confirm</span></span>
<span data-ttu-id="cf0d2-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf0d2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf0d2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf0d2-131">-WhatIf</span></span>
<span data-ttu-id="cf0d2-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf0d2-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf0d2-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cf0d2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf0d2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf0d2-134">CommonParameters</span></span>
<span data-ttu-id="cf0d2-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf0d2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf0d2-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf0d2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf0d2-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf0d2-137">INPUTS</span></span>

### <span data-ttu-id="cf0d2-138">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cf0d2-138">VirtualMachineScaleSet</span></span>
<span data-ttu-id="cf0d2-139">Parametr "VirtualMachineScaleSet" akceptuje wartość typu "VirtualMachineScaleSet" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="cf0d2-139">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="cf0d2-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cf0d2-140">OUTPUTS</span></span>

### <span data-ttu-id="cf0d2-141">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cf0d2-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="cf0d2-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cf0d2-142">NOTES</span></span>

## <span data-ttu-id="cf0d2-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf0d2-143">RELATED LINKS</span></span>

[<span data-ttu-id="cf0d2-144">Nowe — AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="cf0d2-144">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
