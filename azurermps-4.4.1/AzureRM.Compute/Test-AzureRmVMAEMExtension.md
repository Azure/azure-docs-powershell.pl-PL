---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
ms.openlocfilehash: 3c6f1ca4a50ccc359c1bbf10e63c9a9c0baf05fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553962"
---
# <span data-ttu-id="bedbe-101">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="bedbe-101">Test-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="bedbe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bedbe-102">SYNOPSIS</span></span>
<span data-ttu-id="bedbe-103">Sprawdza konfigurację rozszerzenia AEM.</span><span class="sxs-lookup"><span data-stu-id="bedbe-103">Checks the configuration of the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bedbe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bedbe-104">SYNTAX</span></span>

```
Test-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bedbe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bedbe-105">DESCRIPTION</span></span>
<span data-ttu-id="bedbe-106">Polecenie cmdlet **test-AzureRmVMAEMExtension** sprawdza konfigurację rozszerzenia usługi Azure Enhanced Monitoring (AEM).</span><span class="sxs-lookup"><span data-stu-id="bedbe-106">The **Test-AzureRmVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="bedbe-107">Rozszerzenie AEM gromadzi dane dotyczące wydajności.</span><span class="sxs-lookup"><span data-stu-id="bedbe-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="bedbe-108">To polecenie cmdlet sprawdza, czy dane wydajności są dostępne.</span><span class="sxs-lookup"><span data-stu-id="bedbe-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="bedbe-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bedbe-109">EXAMPLES</span></span>

### <span data-ttu-id="bedbe-110">Przykład 1: Sprawdzanie konfiguracji rozszerzenia AEM</span><span class="sxs-lookup"><span data-stu-id="bedbe-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="bedbe-111">To polecenie sprawdza konfigurację rozszerzenia AEM dla maszyny wirtualnej o nazwie contoso — Server.</span><span class="sxs-lookup"><span data-stu-id="bedbe-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="bedbe-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bedbe-112">PARAMETERS</span></span>

### <span data-ttu-id="bedbe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bedbe-113">-DefaultProfile</span></span>
<span data-ttu-id="bedbe-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bedbe-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bedbe-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="bedbe-115">-OSType</span></span>
<span data-ttu-id="bedbe-116">Określa typ systemu operacyjnego dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="bedbe-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="bedbe-117">Jeśli dysk systemu operacyjnego nie ma typu, należy określić ten parametr.</span><span class="sxs-lookup"><span data-stu-id="bedbe-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="bedbe-118">Dopuszczalne wartości tego parametru to: Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="bedbe-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="bedbe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bedbe-119">-ResourceGroupName</span></span>
<span data-ttu-id="bedbe-120">Określa nazwę grupy zasobów maszyny wirtualnej, którą to polecenie cmdlet sprawdza.</span><span class="sxs-lookup"><span data-stu-id="bedbe-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="bedbe-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="bedbe-121">-SkipStorageCheck</span></span>
<span data-ttu-id="bedbe-122">Wskazuje, że to polecenie cmdlet pomija Sprawdzanie konfiguracji magazynu.</span><span class="sxs-lookup"><span data-stu-id="bedbe-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

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

### <span data-ttu-id="bedbe-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="bedbe-123">-VMName</span></span>
<span data-ttu-id="bedbe-124">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bedbe-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="bedbe-125">To polecenie cmdlet testuje rozszerzenie AEM dla maszyny wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="bedbe-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="bedbe-126">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="bedbe-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="bedbe-127">Określa limit czasu (w minutach) sprawdzania konfiguracji magazynu.</span><span class="sxs-lookup"><span data-stu-id="bedbe-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

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

### <span data-ttu-id="bedbe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bedbe-128">CommonParameters</span></span>
<span data-ttu-id="bedbe-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bedbe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bedbe-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bedbe-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bedbe-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bedbe-131">INPUTS</span></span>

## <span data-ttu-id="bedbe-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bedbe-132">OUTPUTS</span></span>

## <span data-ttu-id="bedbe-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bedbe-133">NOTES</span></span>

## <span data-ttu-id="bedbe-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bedbe-134">RELATED LINKS</span></span>

[<span data-ttu-id="bedbe-135">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="bedbe-135">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="bedbe-136">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="bedbe-136">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="bedbe-137">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="bedbe-137">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)


