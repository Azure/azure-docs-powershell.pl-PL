---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
ms.openlocfilehash: 0d7312d7ecbddf15530438e9729e470bd202e488
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717870"
---
# <span data-ttu-id="4f281-101">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="4f281-101">Get-AzureRmVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="4f281-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4f281-102">SYNOPSIS</span></span>
<span data-ttu-id="4f281-103">Pobiera stan szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4f281-103">Gets the encryption status of the virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f281-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4f281-104">SYNTAX</span></span>

```
Get-AzureRmVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f281-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4f281-105">DESCRIPTION</span></span>
<span data-ttu-id="4f281-106">Polecenie cmdlet **Get-AzureRmVMDiskEncryptionStatus** Pobiera stan szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4f281-106">The **Get-AzureRmVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="4f281-107">Wyświetla stan szyfrowania systemu operacyjnego i woluminów danych.</span><span class="sxs-lookup"><span data-stu-id="4f281-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="4f281-108">Oprócz stanu szyfrowania jest również wyświetlany tajny adres URL szyfrowania, adres URL klucza szyfrowania klucza, identyfikatory zasobów **magazynów** kluczy, w których znajdują się klucze szyfrowania i klucz szyfrowania kluczy na woluminie systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="4f281-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="4f281-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4f281-109">EXAMPLES</span></span>

### <span data-ttu-id="4f281-110">Przykład 1: uzyskiwanie stanu szyfrowania maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="4f281-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzureRmVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="4f281-111">To polecenie pobiera stan szyfrowania maszyny wirtualnej o nazwie VM001.</span><span class="sxs-lookup"><span data-stu-id="4f281-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="4f281-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4f281-112">PARAMETERS</span></span>

### <span data-ttu-id="4f281-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f281-113">-DefaultProfile</span></span>
<span data-ttu-id="4f281-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4f281-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f281-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4f281-115">-Name</span></span>
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

### <span data-ttu-id="4f281-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f281-116">-ResourceGroupName</span></span>
<span data-ttu-id="4f281-117">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4f281-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="4f281-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="4f281-118">-VMName</span></span>
<span data-ttu-id="4f281-119">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4f281-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="4f281-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f281-120">CommonParameters</span></span>
<span data-ttu-id="4f281-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f281-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f281-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f281-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f281-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f281-123">INPUTS</span></span>

## <span data-ttu-id="4f281-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4f281-124">OUTPUTS</span></span>

## <span data-ttu-id="4f281-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4f281-125">NOTES</span></span>

## <span data-ttu-id="4f281-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4f281-126">RELATED LINKS</span></span>

[<span data-ttu-id="4f281-127">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="4f281-127">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="4f281-128">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="4f281-128">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


