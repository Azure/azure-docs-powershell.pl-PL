---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermremotedesktopfile
schema: 2.0.0
ms.openlocfilehash: e8b19272ed7b6c68221e34cef0395f0592b3013d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898078"
---
# <span data-ttu-id="a8dd3-101">Get-AzureRmRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="a8dd3-101">Get-AzureRmRemoteDesktopFile</span></span>

## <span data-ttu-id="a8dd3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a8dd3-102">SYNOPSIS</span></span>
<span data-ttu-id="a8dd3-103">Pobiera plik RDP.</span><span class="sxs-lookup"><span data-stu-id="a8dd3-103">Gets an .rdp file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8dd3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a8dd3-104">SYNTAX</span></span>

### <span data-ttu-id="a8dd3-105">Pobierz</span><span class="sxs-lookup"><span data-stu-id="a8dd3-105">Download</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8dd3-106">Wczesn</span><span class="sxs-lookup"><span data-stu-id="a8dd3-106">Launch</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8dd3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a8dd3-107">DESCRIPTION</span></span>
<span data-ttu-id="a8dd3-108">Polecenie cmdlet **Get-AzureRmRemoteDesktopFile** pobiera plik protokołu RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="a8dd3-108">The **Get-AzureRmRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="a8dd3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a8dd3-109">EXAMPLES</span></span>

### <span data-ttu-id="a8dd3-110">Przykład 1: uzyskiwanie pliku pulpitu zdalnego</span><span class="sxs-lookup"><span data-stu-id="a8dd3-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzureRmRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="a8dd3-111">To polecenie pobiera plik pulpitu zdalnego dla maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="a8dd3-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="a8dd3-112">Polecenie zapisuje wynik w pliku o nazwie D:\RemoteDesktopFile07.rdp.</span><span class="sxs-lookup"><span data-stu-id="a8dd3-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="a8dd3-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a8dd3-113">PARAMETERS</span></span>

### <span data-ttu-id="a8dd3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8dd3-114">-DefaultProfile</span></span>
<span data-ttu-id="a8dd3-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a8dd3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8dd3-116">-Uruchom</span><span class="sxs-lookup"><span data-stu-id="a8dd3-116">-Launch</span></span>
<span data-ttu-id="a8dd3-117">Wskazuje, że to polecenie cmdlet uruchamia pulpit zdalny po otrzymaniu pliku RDP.</span><span class="sxs-lookup"><span data-stu-id="a8dd3-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

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

### <span data-ttu-id="a8dd3-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="a8dd3-118">-LocalPath</span></span>
<span data-ttu-id="a8dd3-119">Określa lokalną pełną ścieżkę, w której to polecenie cmdlet przechowuje plik RDP.</span><span class="sxs-lookup"><span data-stu-id="a8dd3-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

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

### <span data-ttu-id="a8dd3-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a8dd3-120">-Name</span></span>
<span data-ttu-id="a8dd3-121">Określa nazwę zestawu dostępności, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8dd3-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a8dd3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8dd3-122">-ResourceGroupName</span></span>
<span data-ttu-id="a8dd3-123">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a8dd3-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a8dd3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8dd3-124">CommonParameters</span></span>
<span data-ttu-id="a8dd3-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8dd3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8dd3-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8dd3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8dd3-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8dd3-127">INPUTS</span></span>

### <span data-ttu-id="a8dd3-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a8dd3-128">None</span></span>
<span data-ttu-id="a8dd3-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="a8dd3-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a8dd3-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a8dd3-130">OUTPUTS</span></span>

## <span data-ttu-id="a8dd3-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a8dd3-131">NOTES</span></span>

## <span data-ttu-id="a8dd3-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8dd3-132">RELATED LINKS</span></span>

