---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
ms.openlocfilehash: 6100a8594b380981bfbfbe25f2334740e915ff2e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717637"
---
# <span data-ttu-id="b4ccc-101">Add-AzureRmVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="b4ccc-101">Add-AzureRmVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="b4ccc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b4ccc-102">SYNOPSIS</span></span>
<span data-ttu-id="b4ccc-103">Dodaje informacje do pliku odpowiedzi instalacji nienadzorowanej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="b4ccc-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4ccc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b4ccc-104">SYNTAX</span></span>

```
Add-AzureRmVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4ccc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b4ccc-105">DESCRIPTION</span></span>
<span data-ttu-id="b4ccc-106">Polecenie cmdlet **Add-AzureRmVmssAdditionalUnattendContent** umożliwia dodanie informacji do pliku odpowiedzi instalacji nienadzorowanej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="b4ccc-106">The **Add-AzureRmVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="b4ccc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b4ccc-107">EXAMPLES</span></span>

### <span data-ttu-id="b4ccc-108">Przykład 1. Dodawanie informacji do pliku odpowiedzi instalacji nienadzorowanej systemu Windows</span><span class="sxs-lookup"><span data-stu-id="b4ccc-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzureRmVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="b4ccc-109">To polecenie umożliwia dodanie informacji do pliku odpowiedzi instalacji nienadzorowanej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="b4ccc-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="b4ccc-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b4ccc-110">PARAMETERS</span></span>

### <span data-ttu-id="b4ccc-111">-Składnikname</span><span class="sxs-lookup"><span data-stu-id="b4ccc-111">-ComponentName</span></span>
<span data-ttu-id="b4ccc-112">Określa nazwę składnika do skonfigurowania przy użyciu dodanej zawartości.</span><span class="sxs-lookup"><span data-stu-id="b4ccc-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="b4ccc-113">Jedyną dozwoloną wartością jest Microsoft-Windows-Shell-Setup.</span><span class="sxs-lookup"><span data-stu-id="b4ccc-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ComponentNames]
Parameter Sets: (All)
Aliases:
Accepted values: MicrosoftWindowsShellSetup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4ccc-114">-Content (zawartość)</span><span class="sxs-lookup"><span data-stu-id="b4ccc-114">-Content</span></span>
<span data-ttu-id="b4ccc-115">Określa zawartość w formacie XML, która jest dodawana do pliku unattend.xml określonej ścieżki i składnika.</span><span class="sxs-lookup"><span data-stu-id="b4ccc-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4ccc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4ccc-116">-DefaultProfile</span></span>
<span data-ttu-id="b4ccc-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4ccc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4ccc-118">-Passname</span><span class="sxs-lookup"><span data-stu-id="b4ccc-118">-PassName</span></span>
<span data-ttu-id="b4ccc-119">Określa nazwę przebiegu, do którego odnosi się zawartość.</span><span class="sxs-lookup"><span data-stu-id="b4ccc-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="b4ccc-120">Jedyną dozwoloną wartością jest oobeSystem.</span><span class="sxs-lookup"><span data-stu-id="b4ccc-120">The only allowable value is oobeSystem.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.PassNames]
Parameter Sets: (All)
Aliases:
Accepted values: OobeSystem

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4ccc-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="b4ccc-121">-SettingName</span></span>
<span data-ttu-id="b4ccc-122">Określa nazwę ustawienia, którego dotyczy zawartość.</span><span class="sxs-lookup"><span data-stu-id="b4ccc-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="b4ccc-123">Dopuszczalne wartości tego parametru to::</span><span class="sxs-lookup"><span data-stu-id="b4ccc-123">The acceptable values for this parameter are::</span></span>
- <span data-ttu-id="b4ccc-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="b4ccc-124">FirstLogonCommands</span></span>
- <span data-ttu-id="b4ccc-125">Autologowanie</span><span class="sxs-lookup"><span data-stu-id="b4ccc-125">AutoLogon</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases:
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4ccc-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b4ccc-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="b4ccc-127">Określ obiekt **zestawu skali** maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b4ccc-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="b4ccc-128">Aby utworzyć obiekt, możesz użyć polecenia cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="b4ccc-128">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4ccc-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b4ccc-129">-Confirm</span></span>
<span data-ttu-id="b4ccc-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4ccc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4ccc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4ccc-131">-WhatIf</span></span>
<span data-ttu-id="b4ccc-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4ccc-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4ccc-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b4ccc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4ccc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4ccc-134">CommonParameters</span></span>
<span data-ttu-id="b4ccc-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4ccc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4ccc-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4ccc-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4ccc-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4ccc-137">INPUTS</span></span>

### <span data-ttu-id="b4ccc-138">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b4ccc-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="b4ccc-139">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. PassNames, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="b4ccc-139">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.PassNames, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="b4ccc-140">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. ComponentNames, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="b4ccc-140">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ComponentNames, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="b4ccc-141">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. SettingNames, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="b4ccc-141">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="b4ccc-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b4ccc-142">System.String</span></span>

## <span data-ttu-id="b4ccc-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b4ccc-143">OUTPUTS</span></span>

### <span data-ttu-id="b4ccc-144">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b4ccc-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="b4ccc-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b4ccc-145">NOTES</span></span>

## <span data-ttu-id="b4ccc-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4ccc-146">RELATED LINKS</span></span>

[<span data-ttu-id="b4ccc-147">Nowe — AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="b4ccc-147">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
