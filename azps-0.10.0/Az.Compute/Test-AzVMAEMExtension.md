---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/test-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Test-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Test-AzVMAEMExtension.md
ms.openlocfilehash: 36fd9813523a5977c1981e6de54384cf71de7dc5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891605"
---
# <span data-ttu-id="db537-101">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="db537-101">Test-AzVMAEMExtension</span></span>

## <span data-ttu-id="db537-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="db537-102">SYNOPSIS</span></span>
<span data-ttu-id="db537-103">Sprawdza konfigurację rozszerzenia AEM.</span><span class="sxs-lookup"><span data-stu-id="db537-103">Checks the configuration of the AEM extension.</span></span>

## <span data-ttu-id="db537-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="db537-104">SYNTAX</span></span>

```
Test-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="db537-105">Opis</span><span class="sxs-lookup"><span data-stu-id="db537-105">DESCRIPTION</span></span>
<span data-ttu-id="db537-106">Polecenie cmdlet **test-AzVMAEMExtension** sprawdza konfigurację rozszerzenia usługi Azure Enhanced Monitoring (AEM).</span><span class="sxs-lookup"><span data-stu-id="db537-106">The **Test-AzVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="db537-107">Rozszerzenie AEM gromadzi dane dotyczące wydajności.</span><span class="sxs-lookup"><span data-stu-id="db537-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="db537-108">To polecenie cmdlet sprawdza, czy dane wydajności są dostępne.</span><span class="sxs-lookup"><span data-stu-id="db537-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="db537-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="db537-109">EXAMPLES</span></span>

### <span data-ttu-id="db537-110">Przykład 1: Sprawdzanie konfiguracji rozszerzenia AEM</span><span class="sxs-lookup"><span data-stu-id="db537-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="db537-111">To polecenie sprawdza konfigurację rozszerzenia AEM dla maszyny wirtualnej o nazwie contoso — Server.</span><span class="sxs-lookup"><span data-stu-id="db537-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="db537-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="db537-112">PARAMETERS</span></span>

### <span data-ttu-id="db537-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db537-113">-DefaultProfile</span></span>
<span data-ttu-id="db537-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="db537-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db537-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="db537-115">-OSType</span></span>
<span data-ttu-id="db537-116">Określa typ systemu operacyjnego dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="db537-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="db537-117">Jeśli dysk systemu operacyjnego nie ma typu, należy określić ten parametr.</span><span class="sxs-lookup"><span data-stu-id="db537-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="db537-118">Dopuszczalne wartości tego parametru to: Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="db537-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db537-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db537-119">-ResourceGroupName</span></span>
<span data-ttu-id="db537-120">Określa nazwę grupy zasobów maszyny wirtualnej, którą to polecenie cmdlet sprawdza.</span><span class="sxs-lookup"><span data-stu-id="db537-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="db537-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="db537-121">-SkipStorageCheck</span></span>
<span data-ttu-id="db537-122">Wskazuje, że to polecenie cmdlet pomija Sprawdzanie konfiguracji magazynu.</span><span class="sxs-lookup"><span data-stu-id="db537-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db537-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="db537-123">-VMName</span></span>
<span data-ttu-id="db537-124">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="db537-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="db537-125">To polecenie cmdlet testuje rozszerzenie AEM dla maszyny wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="db537-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="db537-126">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="db537-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="db537-127">Określa limit czasu (w minutach) sprawdzania konfiguracji magazynu.</span><span class="sxs-lookup"><span data-stu-id="db537-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db537-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db537-128">CommonParameters</span></span>
<span data-ttu-id="db537-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db537-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db537-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db537-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db537-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db537-131">INPUTS</span></span>

### <span data-ttu-id="db537-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="db537-132">None</span></span>
<span data-ttu-id="db537-133">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="db537-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="db537-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="db537-134">OUTPUTS</span></span>

### <span data-ttu-id="db537-135">Microsoft. Azure. Commands. COMPUTE. Extension. AEM. AEMTestResult</span><span class="sxs-lookup"><span data-stu-id="db537-135">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="db537-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="db537-136">NOTES</span></span>

## <span data-ttu-id="db537-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="db537-137">RELATED LINKS</span></span>

[<span data-ttu-id="db537-138">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="db537-138">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="db537-139">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="db537-139">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="db537-140">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="db537-140">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)


