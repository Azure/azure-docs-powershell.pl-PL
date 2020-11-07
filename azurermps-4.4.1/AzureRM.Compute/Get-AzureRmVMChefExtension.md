---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMChefExtension.md
ms.openlocfilehash: 2aa0c6516614adb5fae84e2d141cf1882de71628
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719666"
---
# <span data-ttu-id="34c1e-101">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="34c1e-101">Get-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="34c1e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34c1e-102">SYNOPSIS</span></span>
<span data-ttu-id="34c1e-103">Pobiera informacje o rozszerzeniu Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="34c1e-103">Gets information about a Chef extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34c1e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34c1e-104">SYNTAX</span></span>

### <span data-ttu-id="34c1e-105">Linux</span><span class="sxs-lookup"><span data-stu-id="34c1e-105">Linux</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Linux] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34c1e-106">Microsoft</span><span class="sxs-lookup"><span data-stu-id="34c1e-106">Windows</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Windows] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34c1e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="34c1e-107">DESCRIPTION</span></span>
<span data-ttu-id="34c1e-108">Polecenie cmdlet **Get-AzureVMChefExtension** pobiera informacje o rozszerzeniu Kuchmistrz zainstalowanym na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="34c1e-108">The **Get-AzureVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="34c1e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34c1e-109">EXAMPLES</span></span>

### <span data-ttu-id="34c1e-110">Przykład 1: uzyskiwanie szczegółowych informacji o rozszerzeniu Kuchmistrz dla maszyny wirtualnej systemu Windows</span><span class="sxs-lookup"><span data-stu-id="34c1e-110">Example 1: Get the details of Chef extension for a Windows virtual machine-</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="34c1e-111">To polecenie pobiera rozszerzenie Kuchmistrz z maszyny wirtualnej systemu Windows o nazwie WindowsVM001 należącej do grupy zasobów o nazwie ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="34c1e-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="34c1e-112">Przykład 2: uzyskiwanie szczegółowych informacji o rozszerzeniu Kuchmistrz dla maszyny wirtualnej Linux</span><span class="sxs-lookup"><span data-stu-id="34c1e-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="34c1e-113">To polecenie pobiera rozszerzenie Kuchmistrz z maszyny wirtualnej Linux o nazwie LinuxVM001 należącej do grupy zasobów o nazwie ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="34c1e-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="34c1e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34c1e-114">PARAMETERS</span></span>

### <span data-ttu-id="34c1e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34c1e-115">-DefaultProfile</span></span>
<span data-ttu-id="34c1e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="34c1e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34c1e-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="34c1e-117">-Linux</span></span>
<span data-ttu-id="34c1e-118">Wskazuje, że to polecenie cmdlet działa na maszynie wirtualnej Linux.</span><span class="sxs-lookup"><span data-stu-id="34c1e-118">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34c1e-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="34c1e-119">-Name</span></span>
<span data-ttu-id="34c1e-120">Określa nazwę rozszerzenia Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="34c1e-120">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="34c1e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34c1e-121">-ResourceGroupName</span></span>
<span data-ttu-id="34c1e-122">Określa nazwę grupy zasobów zawierającej maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="34c1e-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="34c1e-123">-Status</span><span class="sxs-lookup"><span data-stu-id="34c1e-123">-Status</span></span>
<span data-ttu-id="34c1e-124">Wskazuje, że to polecenie cmdlet pobiera tylko widok wystąpienia rozszerzenia Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="34c1e-124">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

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

### <span data-ttu-id="34c1e-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="34c1e-125">-VMName</span></span>
<span data-ttu-id="34c1e-126">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="34c1e-126">Specifies the name of a virtual machine.</span></span>

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

### <span data-ttu-id="34c1e-127">-Windows</span><span class="sxs-lookup"><span data-stu-id="34c1e-127">-Windows</span></span>
<span data-ttu-id="34c1e-128">Wskazuje, że to polecenie cmdlet dotyczy maszyny wirtualnej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="34c1e-128">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34c1e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34c1e-129">CommonParameters</span></span>
<span data-ttu-id="34c1e-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34c1e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34c1e-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34c1e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34c1e-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34c1e-132">INPUTS</span></span>

## <span data-ttu-id="34c1e-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34c1e-133">OUTPUTS</span></span>

## <span data-ttu-id="34c1e-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34c1e-134">NOTES</span></span>

## <span data-ttu-id="34c1e-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34c1e-135">RELATED LINKS</span></span>

[<span data-ttu-id="34c1e-136">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="34c1e-136">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)

[<span data-ttu-id="34c1e-137">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="34c1e-137">Remove-AzureRmVMChefExtension</span></span>](./Remove-AzureRmVMChefExtension.md)


