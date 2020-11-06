---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
ms.openlocfilehash: 398cc4b8f23ca5296aec741eb720833f589b0e2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541863"
---
# <span data-ttu-id="5db07-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="5db07-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="5db07-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5db07-102">SYNOPSIS</span></span>
<span data-ttu-id="5db07-103">Pobiera informacje o rozszerzeniu domeny usługi AD.</span><span class="sxs-lookup"><span data-stu-id="5db07-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5db07-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5db07-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5db07-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5db07-105">DESCRIPTION</span></span>
<span data-ttu-id="5db07-106">Polecenie cmdlet **Get-AzureRmVMADDomainExtension** pobiera informacje o określonym rozszerzeniu domeny usługi Azure Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="5db07-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="5db07-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5db07-107">EXAMPLES</span></span>

## <span data-ttu-id="5db07-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5db07-108">PARAMETERS</span></span>

### <span data-ttu-id="5db07-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5db07-109">-DefaultProfile</span></span>
<span data-ttu-id="5db07-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5db07-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5db07-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5db07-111">-Name</span></span>
<span data-ttu-id="5db07-112">Określa nazwę rozszerzenia domeny.</span><span class="sxs-lookup"><span data-stu-id="5db07-112">Specifies the name of the domain extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5db07-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5db07-113">-ResourceGroupName</span></span>
<span data-ttu-id="5db07-114">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5db07-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5db07-115">-Status</span><span class="sxs-lookup"><span data-stu-id="5db07-115">-Status</span></span>
<span data-ttu-id="5db07-116">Wskazuje, że to polecenie cmdlet pobiera widok wystąpienia rozszerzenia domeny.</span><span class="sxs-lookup"><span data-stu-id="5db07-116">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5db07-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="5db07-117">-VMName</span></span>
<span data-ttu-id="5db07-118">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5db07-118">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="5db07-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5db07-119">CommonParameters</span></span>
<span data-ttu-id="5db07-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5db07-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5db07-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5db07-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5db07-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5db07-122">INPUTS</span></span>

### <span data-ttu-id="5db07-123">System. String</span><span class="sxs-lookup"><span data-stu-id="5db07-123">System.String</span></span>

### <span data-ttu-id="5db07-124">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5db07-124">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5db07-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5db07-125">OUTPUTS</span></span>

### <span data-ttu-id="5db07-126">Microsoft. Azure. Commands. COMPUTE. models. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="5db07-126">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="5db07-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5db07-127">NOTES</span></span>

## <span data-ttu-id="5db07-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5db07-128">RELATED LINKS</span></span>

[<span data-ttu-id="5db07-129">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="5db07-129">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)


