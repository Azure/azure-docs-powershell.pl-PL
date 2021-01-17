---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiskencryptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
ms.openlocfilehash: 4ad5ef08f9c12693a2fa4b4b372ee1320f90fb76
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352906"
---
# <span data-ttu-id="d178a-101">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="d178a-101">Get-AzVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="d178a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d178a-102">SYNOPSIS</span></span>
<span data-ttu-id="d178a-103">Pobiera stan szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d178a-103">Gets the encryption status of the virtual machine.</span></span>

## <span data-ttu-id="d178a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d178a-104">SYNTAX</span></span>

```
Get-AzVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d178a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d178a-105">DESCRIPTION</span></span>
<span data-ttu-id="d178a-106">Polecenie cmdlet **Get-AzVMDiskEncryptionStatus** Pobiera stan szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d178a-106">The **Get-AzVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="d178a-107">Wyświetla stan szyfrowania systemu operacyjnego i woluminów danych.</span><span class="sxs-lookup"><span data-stu-id="d178a-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="d178a-108">Oprócz stanu szyfrowania jest również wyświetlany tajny adres URL szyfrowania, adres URL klucza szyfrowania klucza, identyfikatory zasobów **magazynów** kluczy, w których znajdują się klucze szyfrowania i klucz szyfrowania kluczy na woluminie systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="d178a-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="d178a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d178a-109">EXAMPLES</span></span>

### <span data-ttu-id="d178a-110">Przykład 1: uzyskiwanie stanu szyfrowania maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="d178a-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="d178a-111">To polecenie pobiera stan szyfrowania maszyny wirtualnej o nazwie VM001.</span><span class="sxs-lookup"><span data-stu-id="d178a-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="d178a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d178a-112">PARAMETERS</span></span>

### <span data-ttu-id="d178a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d178a-113">-DefaultProfile</span></span>
<span data-ttu-id="d178a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d178a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d178a-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="d178a-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="d178a-116">Nazwa wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="d178a-116">The extension publisher name.</span></span> <span data-ttu-id="d178a-117">Ten parametr można określić tylko w celu zastąpienia wartości domyślnej "Microsoft. Azure. Security".</span><span class="sxs-lookup"><span data-stu-id="d178a-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="d178a-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="d178a-118">-ExtensionType</span></span>
<span data-ttu-id="d178a-119">Typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="d178a-119">The extension type.</span></span> <span data-ttu-id="d178a-120">Określ ten parametr, aby zastąpić swoją domyślną wartość "AzureDiskEncryption" dla maszyn wirtualnych systemu Windows i "AzureDiskEncryptionForLinux" dla maszyn wirtualnych Linux.</span><span class="sxs-lookup"><span data-stu-id="d178a-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="d178a-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d178a-121">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d178a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d178a-122">-ResourceGroupName</span></span>
<span data-ttu-id="d178a-123">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d178a-123">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d178a-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="d178a-124">-VMName</span></span>
<span data-ttu-id="d178a-125">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d178a-125">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d178a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d178a-126">CommonParameters</span></span>
<span data-ttu-id="d178a-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d178a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d178a-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d178a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d178a-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d178a-129">INPUTS</span></span>

### <span data-ttu-id="d178a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d178a-130">System.String</span></span>

## <span data-ttu-id="d178a-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d178a-131">OUTPUTS</span></span>

### <span data-ttu-id="d178a-132">Microsoft. Azure. Commands. COMPUTE. Extension. AzureDiskEncryption. AzureDiskEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="d178a-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="d178a-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d178a-133">NOTES</span></span>

## <span data-ttu-id="d178a-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d178a-134">RELATED LINKS</span></span>

[<span data-ttu-id="d178a-135">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="d178a-135">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="d178a-136">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="d178a-136">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


