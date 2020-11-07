---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmRemoteDesktopFile.md
ms.openlocfilehash: f4b29849109959a8b06a8d0339c8927b8a840a7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717227"
---
# <span data-ttu-id="57a83-101">Get-AzureRmRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="57a83-101">Get-AzureRmRemoteDesktopFile</span></span>

## <span data-ttu-id="57a83-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="57a83-102">SYNOPSIS</span></span>
<span data-ttu-id="57a83-103">Pobiera plik RDP.</span><span class="sxs-lookup"><span data-stu-id="57a83-103">Gets an .rdp file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57a83-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="57a83-104">SYNTAX</span></span>

### <span data-ttu-id="57a83-105">Pobierz</span><span class="sxs-lookup"><span data-stu-id="57a83-105">Download</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [<CommonParameters>]
```

### <span data-ttu-id="57a83-106">Wczesn</span><span class="sxs-lookup"><span data-stu-id="57a83-106">Launch</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [<CommonParameters>]
```

## <span data-ttu-id="57a83-107">Opis</span><span class="sxs-lookup"><span data-stu-id="57a83-107">DESCRIPTION</span></span>
<span data-ttu-id="57a83-108">Polecenie cmdlet **Get-AzureRmRemoteDesktopFile** pobiera plik protokołu RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="57a83-108">The **Get-AzureRmRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="57a83-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="57a83-109">EXAMPLES</span></span>

### <span data-ttu-id="57a83-110">Przykład 1: uzyskiwanie pliku pulpitu zdalnego</span><span class="sxs-lookup"><span data-stu-id="57a83-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzureRmRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="57a83-111">To polecenie pobiera plik pulpitu zdalnego dla maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="57a83-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="57a83-112">Polecenie zapisuje wynik w pliku o nazwie D:\RemoteDesktopFile07.rdp.</span><span class="sxs-lookup"><span data-stu-id="57a83-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="57a83-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="57a83-113">PARAMETERS</span></span>

### <span data-ttu-id="57a83-114">-Uruchom</span><span class="sxs-lookup"><span data-stu-id="57a83-114">-Launch</span></span>
<span data-ttu-id="57a83-115">Wskazuje, że to polecenie cmdlet uruchamia pulpit zdalny po otrzymaniu pliku RDP.</span><span class="sxs-lookup"><span data-stu-id="57a83-115">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Launch
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57a83-116">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="57a83-116">-LocalPath</span></span>
<span data-ttu-id="57a83-117">Określa lokalną pełną ścieżkę, w której to polecenie cmdlet przechowuje plik RDP.</span><span class="sxs-lookup"><span data-stu-id="57a83-117">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

```yaml
Type: String
Parameter Sets: Download
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Launch
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57a83-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="57a83-118">-Name</span></span>
<span data-ttu-id="57a83-119">Określa nazwę zestawu dostępności, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57a83-119">Specifies the name of the availability set that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57a83-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57a83-120">-ResourceGroupName</span></span>
<span data-ttu-id="57a83-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="57a83-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="57a83-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57a83-122">CommonParameters</span></span>
<span data-ttu-id="57a83-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57a83-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57a83-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57a83-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57a83-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57a83-125">INPUTS</span></span>

### <span data-ttu-id="57a83-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="57a83-126">None</span></span>
<span data-ttu-id="57a83-127">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="57a83-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="57a83-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="57a83-128">OUTPUTS</span></span>

## <span data-ttu-id="57a83-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="57a83-129">NOTES</span></span>

## <span data-ttu-id="57a83-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57a83-130">RELATED LINKS</span></span>

