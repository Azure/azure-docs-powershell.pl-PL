---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
ms.openlocfilehash: ca6b3d4863629aa94585db9850042fff4165dd10
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94054032"
---
# <span data-ttu-id="5ebab-101">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="5ebab-101">Get-AzVMADDomainExtension</span></span>

## <span data-ttu-id="5ebab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ebab-102">SYNOPSIS</span></span>
<span data-ttu-id="5ebab-103">Pobiera informacje o rozszerzeniu domeny usługi AD.</span><span class="sxs-lookup"><span data-stu-id="5ebab-103">Gets information about an AD domain extension.</span></span>

## <span data-ttu-id="5ebab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ebab-104">SYNTAX</span></span>

```
Get-AzVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ebab-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5ebab-105">DESCRIPTION</span></span>
<span data-ttu-id="5ebab-106">Polecenie cmdlet **Get-AzVMADDomainExtension** pobiera informacje o określonym rozszerzeniu domeny usługi Azure Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="5ebab-106">The **Get-AzVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="5ebab-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ebab-107">EXAMPLES</span></span>

## <span data-ttu-id="5ebab-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ebab-108">PARAMETERS</span></span>

### <span data-ttu-id="5ebab-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ebab-109">-DefaultProfile</span></span>
<span data-ttu-id="5ebab-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ebab-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ebab-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5ebab-111">-Name</span></span>
<span data-ttu-id="5ebab-112">Określa nazwę rozszerzenia domeny.</span><span class="sxs-lookup"><span data-stu-id="5ebab-112">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="5ebab-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ebab-113">-ResourceGroupName</span></span>
<span data-ttu-id="5ebab-114">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ebab-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5ebab-115">-Status</span><span class="sxs-lookup"><span data-stu-id="5ebab-115">-Status</span></span>
<span data-ttu-id="5ebab-116">Wskazuje, że to polecenie cmdlet pobiera widok wystąpienia rozszerzenia domeny.</span><span class="sxs-lookup"><span data-stu-id="5ebab-116">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="5ebab-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="5ebab-117">-VMName</span></span>
<span data-ttu-id="5ebab-118">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5ebab-118">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="5ebab-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ebab-119">CommonParameters</span></span>
<span data-ttu-id="5ebab-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ebab-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ebab-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ebab-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ebab-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ebab-122">INPUTS</span></span>

### <span data-ttu-id="5ebab-123">System. String</span><span class="sxs-lookup"><span data-stu-id="5ebab-123">System.String</span></span>

### <span data-ttu-id="5ebab-124">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5ebab-124">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5ebab-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ebab-125">OUTPUTS</span></span>

### <span data-ttu-id="5ebab-126">Microsoft. Azure. Commands. COMPUTE. models. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="5ebab-126">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="5ebab-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ebab-127">NOTES</span></span>

## <span data-ttu-id="5ebab-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ebab-128">RELATED LINKS</span></span>

[<span data-ttu-id="5ebab-129">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="5ebab-129">Set-AzVMADDomainExtension</span></span>](./Set-AzVMADDomainExtension.md)


