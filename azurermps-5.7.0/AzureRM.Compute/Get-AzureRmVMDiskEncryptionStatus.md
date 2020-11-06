---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
ms.openlocfilehash: 9ec94d0c11bf9302156355c28566ce16f48ae148
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545792"
---
# <span data-ttu-id="0dbca-101">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="0dbca-101">Get-AzureRmVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="0dbca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0dbca-102">SYNOPSIS</span></span>
<span data-ttu-id="0dbca-103">Pobiera stan szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0dbca-103">Gets the encryption status of the virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0dbca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0dbca-104">SYNTAX</span></span>

```
Get-AzureRmVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="0dbca-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0dbca-105">DESCRIPTION</span></span>
<span data-ttu-id="0dbca-106">Polecenie cmdlet **Get-AzureRmVMDiskEncryptionStatus** Pobiera stan szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0dbca-106">The **Get-AzureRmVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="0dbca-107">Wyświetla stan szyfrowania systemu operacyjnego i woluminów danych.</span><span class="sxs-lookup"><span data-stu-id="0dbca-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="0dbca-108">Oprócz stanu szyfrowania jest również wyświetlany tajny adres URL szyfrowania, adres URL klucza szyfrowania klucza, identyfikatory zasobów **magazynów** kluczy, w których znajdują się klucze szyfrowania i klucz szyfrowania kluczy na woluminie systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="0dbca-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="0dbca-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0dbca-109">EXAMPLES</span></span>

### <span data-ttu-id="0dbca-110">Przykład 1: uzyskiwanie stanu szyfrowania maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="0dbca-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzureRmVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="0dbca-111">To polecenie pobiera stan szyfrowania maszyny wirtualnej o nazwie VM001.</span><span class="sxs-lookup"><span data-stu-id="0dbca-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="0dbca-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0dbca-112">PARAMETERS</span></span>

### <span data-ttu-id="0dbca-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0dbca-113">-Name</span></span>
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

### <span data-ttu-id="0dbca-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dbca-114">-ResourceGroupName</span></span>
<span data-ttu-id="0dbca-115">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0dbca-115">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0dbca-116">-VMName</span><span class="sxs-lookup"><span data-stu-id="0dbca-116">-VMName</span></span>
<span data-ttu-id="0dbca-117">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0dbca-117">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="0dbca-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dbca-118">CommonParameters</span></span>
<span data-ttu-id="0dbca-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dbca-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dbca-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dbca-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dbca-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0dbca-121">INPUTS</span></span>

### <span data-ttu-id="0dbca-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0dbca-122">None</span></span>
<span data-ttu-id="0dbca-123">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="0dbca-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0dbca-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0dbca-124">OUTPUTS</span></span>

## <span data-ttu-id="0dbca-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0dbca-125">NOTES</span></span>

## <span data-ttu-id="0dbca-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0dbca-126">RELATED LINKS</span></span>

[<span data-ttu-id="0dbca-127">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="0dbca-127">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="0dbca-128">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="0dbca-128">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


