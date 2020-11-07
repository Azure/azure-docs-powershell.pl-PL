---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
ms.openlocfilehash: fd401aa80f65888bc0540bb7975263108e0f8637
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716751"
---
# <span data-ttu-id="eb95e-101">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="eb95e-101">Get-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="eb95e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eb95e-102">SYNOPSIS</span></span>
<span data-ttu-id="eb95e-103">Pobiera ustawienia rozszerzenia diagnostycznego na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="eb95e-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb95e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eb95e-104">SYNTAX</span></span>

```
Get-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb95e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eb95e-105">DESCRIPTION</span></span>
<span data-ttu-id="eb95e-106">Polecenie cmdlet **Get-AzureRmVMDiagnosticsExtension** pobiera ustawienia rozszerzenia Diagnostyka platformy Azure na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="eb95e-106">The **Get-AzureRmVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="eb95e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eb95e-107">EXAMPLES</span></span>

### <span data-ttu-id="eb95e-108">Przykład 1: uzyskiwanie rozszerzenia diagnostycznego zastosowanego do maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="eb95e-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="eb95e-109">To polecenie powoduje wyświetlenie rozszerzenia diagnostycznego zastosowanego do maszyny wirtualnej o nazwie ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="eb95e-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="eb95e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eb95e-110">PARAMETERS</span></span>

### <span data-ttu-id="eb95e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb95e-111">-DefaultProfile</span></span>
<span data-ttu-id="eb95e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eb95e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb95e-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eb95e-113">-Name</span></span>
<span data-ttu-id="eb95e-114">Określa nazwę rozszerzenia diagnostycznego, dla którego to polecenie cmdlet pobiera ustawienia.</span><span class="sxs-lookup"><span data-stu-id="eb95e-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

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

### <span data-ttu-id="eb95e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb95e-115">-ResourceGroupName</span></span>
<span data-ttu-id="eb95e-116">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="eb95e-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="eb95e-117">-Status</span><span class="sxs-lookup"><span data-stu-id="eb95e-117">-Status</span></span>
<span data-ttu-id="eb95e-118">Wskazuje, że w tym poleceniu cmdlet jest używana wartość stanu.</span><span class="sxs-lookup"><span data-stu-id="eb95e-118">Indicates that this cmdlet uses the Status value.</span></span>

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

### <span data-ttu-id="eb95e-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="eb95e-119">-VMName</span></span>
<span data-ttu-id="eb95e-120">Określa nazwę maszyny wirtualnej, z której to polecenie cmdlet uzyskuje rozszerzenie diagnostyczne.</span><span class="sxs-lookup"><span data-stu-id="eb95e-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="eb95e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb95e-121">CommonParameters</span></span>
<span data-ttu-id="eb95e-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb95e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb95e-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb95e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb95e-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb95e-124">INPUTS</span></span>

## <span data-ttu-id="eb95e-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eb95e-125">OUTPUTS</span></span>

## <span data-ttu-id="eb95e-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eb95e-126">NOTES</span></span>

## <span data-ttu-id="eb95e-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eb95e-127">RELATED LINKS</span></span>

[<span data-ttu-id="eb95e-128">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="eb95e-128">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="eb95e-129">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="eb95e-129">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)


