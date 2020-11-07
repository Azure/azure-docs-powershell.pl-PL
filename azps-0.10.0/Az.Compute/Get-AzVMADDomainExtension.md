---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
ms.openlocfilehash: 809246520c4e6b07a1aca406ef3ec17eb9df31f1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893786"
---
# <span data-ttu-id="c34c6-101">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="c34c6-101">Get-AzVMADDomainExtension</span></span>

## <span data-ttu-id="c34c6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c34c6-102">SYNOPSIS</span></span>
<span data-ttu-id="c34c6-103">Pobiera informacje o rozszerzeniu domeny usługi AD.</span><span class="sxs-lookup"><span data-stu-id="c34c6-103">Gets information about an AD domain extension.</span></span>

## <span data-ttu-id="c34c6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c34c6-104">SYNTAX</span></span>

```
Get-AzVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c34c6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c34c6-105">DESCRIPTION</span></span>
<span data-ttu-id="c34c6-106">Polecenie cmdlet **Get-AzVMADDomainExtension** pobiera informacje o określonym rozszerzeniu domeny usługi Azure Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="c34c6-106">The **Get-AzVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="c34c6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c34c6-107">EXAMPLES</span></span>

### <span data-ttu-id="c34c6-108">1:1</span><span class="sxs-lookup"><span data-stu-id="c34c6-108">1:</span></span>
```

```

## <span data-ttu-id="c34c6-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c34c6-109">PARAMETERS</span></span>

### <span data-ttu-id="c34c6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c34c6-110">-DefaultProfile</span></span>
<span data-ttu-id="c34c6-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c34c6-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c34c6-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c34c6-112">-Name</span></span>
<span data-ttu-id="c34c6-113">Określa nazwę rozszerzenia domeny.</span><span class="sxs-lookup"><span data-stu-id="c34c6-113">Specifies the name of the domain extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c34c6-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c34c6-114">-ResourceGroupName</span></span>
<span data-ttu-id="c34c6-115">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c34c6-115">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c34c6-116">-Status</span><span class="sxs-lookup"><span data-stu-id="c34c6-116">-Status</span></span>
<span data-ttu-id="c34c6-117">Wskazuje, że to polecenie cmdlet pobiera widok wystąpienia rozszerzenia domeny.</span><span class="sxs-lookup"><span data-stu-id="c34c6-117">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c34c6-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="c34c6-118">-VMName</span></span>
<span data-ttu-id="c34c6-119">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c34c6-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="c34c6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c34c6-120">CommonParameters</span></span>
<span data-ttu-id="c34c6-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c34c6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c34c6-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c34c6-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c34c6-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c34c6-123">INPUTS</span></span>

### <span data-ttu-id="c34c6-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c34c6-124">None</span></span>
<span data-ttu-id="c34c6-125">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="c34c6-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c34c6-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c34c6-126">OUTPUTS</span></span>

### <span data-ttu-id="c34c6-127">Microsoft. Azure. Commands. COMPUTE. models. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="c34c6-127">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="c34c6-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c34c6-128">NOTES</span></span>

## <span data-ttu-id="c34c6-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c34c6-129">RELATED LINKS</span></span>

[<span data-ttu-id="c34c6-130">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="c34c6-130">Set-AzVMADDomainExtension</span></span>](./Set-AzVMADDomainExtension.md)


