---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/powershell/module/az.compute/test-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
ms.openlocfilehash: 040e7e557934fc90e5609a42c2e553ccf34d2f8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010778"
---
# <span data-ttu-id="d18cf-101">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d18cf-101">Test-AzVMAEMExtension</span></span>

## <span data-ttu-id="d18cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d18cf-102">SYNOPSIS</span></span>
<span data-ttu-id="d18cf-103">Sprawdza konfigurację rozszerzenia AEM.</span><span class="sxs-lookup"><span data-stu-id="d18cf-103">Checks the configuration of the AEM extension.</span></span>

## <span data-ttu-id="d18cf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d18cf-104">SYNTAX</span></span>

```
Test-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d18cf-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d18cf-105">DESCRIPTION</span></span>
<span data-ttu-id="d18cf-106">Polecenie **cmdlet Test-AzVMAEMExtension** sprawdza konfigurację rozszerzenia Azure Enhanced Monitoring (AEM).</span><span class="sxs-lookup"><span data-stu-id="d18cf-106">The **Test-AzVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="d18cf-107">Rozszerzenie AEM gromadzi dane dotyczące wydajności.</span><span class="sxs-lookup"><span data-stu-id="d18cf-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="d18cf-108">To polecenie cmdlet sprawdza, czy dane dotyczące wydajności są dostępne.</span><span class="sxs-lookup"><span data-stu-id="d18cf-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="d18cf-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d18cf-109">EXAMPLES</span></span>

### <span data-ttu-id="d18cf-110">Przykład 1. Sprawdzanie konfiguracji rozszerzenia AEM</span><span class="sxs-lookup"><span data-stu-id="d18cf-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="d18cf-111">To polecenie sprawdza konfigurację rozszerzenia AEM dla maszyny wirtualnej o nazwie contoso-server.</span><span class="sxs-lookup"><span data-stu-id="d18cf-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="d18cf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d18cf-112">PARAMETERS</span></span>

### <span data-ttu-id="d18cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d18cf-113">-DefaultProfile</span></span>
<span data-ttu-id="d18cf-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d18cf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d18cf-115">- OSType</span><span class="sxs-lookup"><span data-stu-id="d18cf-115">-OSType</span></span>
<span data-ttu-id="d18cf-116">Określa typ systemu operacyjnego dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="d18cf-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="d18cf-117">Jeśli dysk systemu operacyjnego nie ma typu, musisz określić ten parametr.</span><span class="sxs-lookup"><span data-stu-id="d18cf-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="d18cf-118">Dopuszczalne wartości dla tego parametru to: Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="d18cf-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18cf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d18cf-119">-ResourceGroupName</span></span>
<span data-ttu-id="d18cf-120">Określa nazwę grupy zasobów maszyny wirtualnej sprawdzaną przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d18cf-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="d18cf-121">- SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="d18cf-121">-SkipStorageCheck</span></span>
<span data-ttu-id="d18cf-122">Wskazuje, że to polecenie cmdlet pomija sprawdzanie konfiguracji magazynu.</span><span class="sxs-lookup"><span data-stu-id="d18cf-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18cf-123">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="d18cf-123">-VMName</span></span>
<span data-ttu-id="d18cf-124">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d18cf-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d18cf-125">To polecenie cmdlet sprawdza rozszerzenie AEM dla maszyny wirtualnej, która określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="d18cf-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="d18cf-126">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="d18cf-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="d18cf-127">Określa, w minutach, okres, przez który jest sprawdzana konfiguracja magazynu.</span><span class="sxs-lookup"><span data-stu-id="d18cf-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18cf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d18cf-128">CommonParameters</span></span>
<span data-ttu-id="d18cf-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d18cf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d18cf-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d18cf-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d18cf-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d18cf-131">INPUTS</span></span>

### <span data-ttu-id="d18cf-132">System.String</span><span class="sxs-lookup"><span data-stu-id="d18cf-132">System.String</span></span>

## <span data-ttu-id="d18cf-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d18cf-133">OUTPUTS</span></span>

### <span data-ttu-id="d18cf-134">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span><span class="sxs-lookup"><span data-stu-id="d18cf-134">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="d18cf-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d18cf-135">NOTES</span></span>

## <span data-ttu-id="d18cf-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d18cf-136">RELATED LINKS</span></span>

[<span data-ttu-id="d18cf-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d18cf-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="d18cf-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d18cf-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="d18cf-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d18cf-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)


