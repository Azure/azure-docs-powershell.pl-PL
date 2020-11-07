---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdiskencryptionextension
schema: 2.0.0
ms.openlocfilehash: 6c580b862ed2c8a420e8f203131ff9d18d187443
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898792"
---
# <span data-ttu-id="8cc91-101">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="8cc91-101">Remove-AzureRmVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="8cc91-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8cc91-102">SYNOPSIS</span></span>
<span data-ttu-id="8cc91-103">Usuwa rozszerzenie szyfrowania dysku z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8cc91-103">Removes the disk encryption extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cc91-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8cc91-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cc91-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8cc91-105">DESCRIPTION</span></span>
<span data-ttu-id="8cc91-106">Polecenie cmdlet **Remove-AzureRmVMDiskEncryptionExtension** usuwa rozszerzenie szyfrowanie dysku z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8cc91-106">The **Remove-AzureRmVMDiskEncryptionExtension** cmdlet removes the disk encryption extension from a virtual machine.</span></span>
<span data-ttu-id="8cc91-107">Jeśli nie podano nazwy rozszerzenia, to polecenie cmdlet usunie rozszerzenie o nazwie domyślnej AzureDiskEncryption dla maszyn wirtualnych z uruchomionym systemem operacyjnym Windows lub AzureDiskEncryptionForLinux dla maszyn wirtualnych opartych na systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="8cc91-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span>
<span data-ttu-id="8cc91-108">To polecenie cmdlet nie wyłącza szyfrowania na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8cc91-108">This cmdlet does not disable encryption on the virtual machine.</span></span>
<span data-ttu-id="8cc91-109">Spowoduje to usunięcie rozszerzenia i skojarzonej z nim konfiguracji rozszerzenia z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8cc91-109">It removes the extension and the associated extension configuration from the virtual machine.</span></span>

## <span data-ttu-id="8cc91-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8cc91-110">EXAMPLES</span></span>

### <span data-ttu-id="8cc91-111">Przykład 1: usunięcie rozszerzenia szyfrowanie dysku z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8cc91-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="8cc91-112">To polecenie usuwa rozszerzenie o nazwie domyślnej AzureDiskEncryption dla maszyny wirtualnej z uruchomionym systemem operacyjnym Windows lub AzureDiskEncryptionForLinux dla maszyny wirtualnej opartej na usłudze Linux o nazwie MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="8cc91-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="8cc91-113">Przykład 2: usunięcie określonego rozszerzenia szyfrowania dysku z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8cc91-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="8cc91-114">To polecenie usuwa rozszerzenie szyfrowania o nazwie MyDiskEncryptionExtension z maszyny wirtualnej o nazwie MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="8cc91-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="8cc91-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8cc91-115">PARAMETERS</span></span>

### <span data-ttu-id="8cc91-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cc91-116">-DefaultProfile</span></span>
<span data-ttu-id="8cc91-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc91-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cc91-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8cc91-118">-Force</span></span>
<span data-ttu-id="8cc91-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8cc91-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cc91-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8cc91-120">-Name</span></span>
<span data-ttu-id="8cc91-121">Określa nazwę zasobu Menedżera zasobów Azure, który reprezentuje rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="8cc91-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="8cc91-122">Polecenie cmdlet Set-AzureRmVMDiskEncryptionExtension ustawia tę nazwę na AzureDiskEncryption dla maszyn wirtualnych z uruchomionym systemem operacyjnym Windows i AzureDiskEncryptionForLinux dla maszyn wirtualnych systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="8cc91-122">The Set-AzureRmVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="8cc91-123">Ten parametr należy określić tylko w przypadku zmiany nazwy domyślnej w poleceniu cmdlet **Set-AzureRmVMDiskEncryptionExtension** lub użycia innej nazwy zasobu w szablonie Menedżera zasobów.</span><span class="sxs-lookup"><span data-stu-id="8cc91-123">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cc91-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cc91-124">-ResourceGroupName</span></span>
<span data-ttu-id="8cc91-125">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8cc91-125">Specifies the name of the resource group for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cc91-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="8cc91-126">-VMName</span></span>
<span data-ttu-id="8cc91-127">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8cc91-127">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cc91-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8cc91-128">-Confirm</span></span>
<span data-ttu-id="8cc91-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cc91-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cc91-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cc91-130">-WhatIf</span></span>
<span data-ttu-id="8cc91-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cc91-131">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="8cc91-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8cc91-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cc91-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cc91-133">CommonParameters</span></span>
<span data-ttu-id="8cc91-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cc91-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cc91-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cc91-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cc91-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8cc91-136">INPUTS</span></span>

### <span data-ttu-id="8cc91-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8cc91-137">None</span></span>
<span data-ttu-id="8cc91-138">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="8cc91-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8cc91-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8cc91-139">OUTPUTS</span></span>

### <span data-ttu-id="8cc91-140">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8cc91-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="8cc91-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8cc91-141">NOTES</span></span>

## <span data-ttu-id="8cc91-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8cc91-142">RELATED LINKS</span></span>

[<span data-ttu-id="8cc91-143">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="8cc91-143">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="8cc91-144">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="8cc91-144">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


