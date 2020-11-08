---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
ms.openlocfilehash: 650602ef229dd6c7371c6befebbb15dacae1d706
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062918"
---
# <span data-ttu-id="c88d3-101">Get-AzRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="c88d3-101">Get-AzRemoteDesktopFile</span></span>

## <span data-ttu-id="c88d3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c88d3-102">SYNOPSIS</span></span>
<span data-ttu-id="c88d3-103">Pobiera plik RDP.</span><span class="sxs-lookup"><span data-stu-id="c88d3-103">Gets an .rdp file.</span></span>

## <span data-ttu-id="c88d3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c88d3-104">SYNTAX</span></span>

### <span data-ttu-id="c88d3-105">Pobierz</span><span class="sxs-lookup"><span data-stu-id="c88d3-105">Download</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c88d3-106">Wczesn</span><span class="sxs-lookup"><span data-stu-id="c88d3-106">Launch</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c88d3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c88d3-107">DESCRIPTION</span></span>
<span data-ttu-id="c88d3-108">Polecenie cmdlet **Get-AzRemoteDesktopFile** pobiera plik protokołu RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="c88d3-108">The **Get-AzRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="c88d3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c88d3-109">EXAMPLES</span></span>

### <span data-ttu-id="c88d3-110">Przykład 1: uzyskiwanie pliku pulpitu zdalnego</span><span class="sxs-lookup"><span data-stu-id="c88d3-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="c88d3-111">To polecenie pobiera plik pulpitu zdalnego dla maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="c88d3-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="c88d3-112">Polecenie zapisuje wynik w pliku o nazwie D:\RemoteDesktopFile07.rdp.</span><span class="sxs-lookup"><span data-stu-id="c88d3-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="c88d3-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c88d3-113">PARAMETERS</span></span>

### <span data-ttu-id="c88d3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c88d3-114">-DefaultProfile</span></span>
<span data-ttu-id="c88d3-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c88d3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c88d3-116">-Uruchom</span><span class="sxs-lookup"><span data-stu-id="c88d3-116">-Launch</span></span>
<span data-ttu-id="c88d3-117">Wskazuje, że to polecenie cmdlet uruchamia pulpit zdalny po otrzymaniu pliku RDP.</span><span class="sxs-lookup"><span data-stu-id="c88d3-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Launch
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88d3-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="c88d3-118">-LocalPath</span></span>
<span data-ttu-id="c88d3-119">Określa lokalną pełną ścieżkę, w której to polecenie cmdlet przechowuje plik RDP.</span><span class="sxs-lookup"><span data-stu-id="c88d3-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Download
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Launch
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c88d3-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c88d3-120">-Name</span></span>
<span data-ttu-id="c88d3-121">Określa nazwę zestawu dostępności, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c88d3-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c88d3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c88d3-122">-ResourceGroupName</span></span>
<span data-ttu-id="c88d3-123">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c88d3-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c88d3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c88d3-124">CommonParameters</span></span>
<span data-ttu-id="c88d3-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c88d3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c88d3-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c88d3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c88d3-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c88d3-127">INPUTS</span></span>

### <span data-ttu-id="c88d3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c88d3-128">System.String</span></span>

## <span data-ttu-id="c88d3-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c88d3-129">OUTPUTS</span></span>

### <span data-ttu-id="c88d3-130">System. void</span><span class="sxs-lookup"><span data-stu-id="c88d3-130">System.Void</span></span>

## <span data-ttu-id="c88d3-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c88d3-131">NOTES</span></span>

## <span data-ttu-id="c88d3-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c88d3-132">RELATED LINKS</span></span>
