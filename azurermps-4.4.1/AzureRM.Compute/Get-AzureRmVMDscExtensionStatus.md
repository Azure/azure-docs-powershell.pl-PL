---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
ms.openlocfilehash: 0a14bf4f2c8a4b686f222079cadaec1744e41d08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550051"
---
# <span data-ttu-id="c4753-101">Get-AzureRmVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="c4753-101">Get-AzureRmVMDscExtensionStatus</span></span>

## <span data-ttu-id="c4753-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c4753-102">SYNOPSIS</span></span>
<span data-ttu-id="c4753-103">Pobiera stan obsługi rozszerzeń DSC dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c4753-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4753-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c4753-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4753-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c4753-105">DESCRIPTION</span></span>
<span data-ttu-id="c4753-106">Polecenie cmdlet **Get-AzureRmVMDscExtensionStatus** Pobiera stan programu obsługi rozszerzeń konfiguracji stanu (DSC) dla maszyny wirtualnej w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="c4753-106">The **Get-AzureRmVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="c4753-107">Po zastosowaniu konfiguracji to polecenie cmdlet zapewnia spójność danych wyjściowych za pomocą polecenia cmdlet Start-DscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c4753-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="c4753-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c4753-108">EXAMPLES</span></span>

## <span data-ttu-id="c4753-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c4753-109">PARAMETERS</span></span>

### <span data-ttu-id="c4753-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4753-110">-DefaultProfile</span></span>
<span data-ttu-id="c4753-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c4753-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4753-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c4753-112">-Name</span></span>
<span data-ttu-id="c4753-113">Określa nazwę zasobu Menedżera zasobów Azure, który reprezentuje rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="c4753-113">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="c4753-114">Polecenie cmdlet Set-AzureRmVMDscExtension powoduje ustawienie tej nazwy na Microsoft. PowerShell. DSC, która jest taka sama, jak wartość używana przez polecenie **Get-AzureRmVMDscExtensionStatus**.</span><span class="sxs-lookup"><span data-stu-id="c4753-114">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtensionStatus**.</span></span>
<span data-ttu-id="c4753-115">Ten parametr należy określić tylko wtedy, gdy w szablonie Menedżera zasobów zmieniono nazwę domyślną w polu Set cmdlet lub użyto innej nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="c4753-115">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4753-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4753-116">-ResourceGroupName</span></span>
<span data-ttu-id="c4753-117">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c4753-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c4753-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="c4753-118">-VMName</span></span>
<span data-ttu-id="c4753-119">Określa nazwę maszyny wirtualnej, dla której to polecenie cmdlet pobiera stan rozszerzenia DSC.</span><span class="sxs-lookup"><span data-stu-id="c4753-119">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4753-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4753-120">CommonParameters</span></span>
<span data-ttu-id="c4753-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4753-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4753-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4753-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4753-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4753-123">INPUTS</span></span>

## <span data-ttu-id="c4753-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c4753-124">OUTPUTS</span></span>

## <span data-ttu-id="c4753-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c4753-125">NOTES</span></span>

## <span data-ttu-id="c4753-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c4753-126">RELATED LINKS</span></span>

[<span data-ttu-id="c4753-127">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="c4753-127">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


