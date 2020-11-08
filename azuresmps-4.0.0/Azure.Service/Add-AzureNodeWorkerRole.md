---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7190C668-6A0C-4E1D-9B5A-0CEEF53E3F85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93573caf43a6c711e1aa1308c851c82faaef5bcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055355"
---
# <span data-ttu-id="13ec1-101">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="13ec1-101">Add-AzureNodeWorkerRole</span></span>

## <span data-ttu-id="13ec1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13ec1-102">SYNOPSIS</span></span>
<span data-ttu-id="13ec1-103">Tworzy wymagane pliki i foldery aplikacji Node.js, która ma być hostowana w chmurze za pośrednictwem node.exe</span><span class="sxs-lookup"><span data-stu-id="13ec1-103">Creates the required files and folders for a Node.js application to be hosted in the cloud via node.exe</span></span>

## <span data-ttu-id="13ec1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13ec1-104">SYNTAX</span></span>

```
Add-AzureNodeWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="13ec1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="13ec1-105">DESCRIPTION</span></span>
<span data-ttu-id="13ec1-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="13ec1-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="13ec1-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="13ec1-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="13ec1-108">Polecenie cmdlet **Add-AzureNodeWorkerRole** tworzy wymagane pliki i foldery, czasami nazywane rusztowaniem, aby aplikacja Node.js mogła być hostowana w chmurze za pośrednictwem node.exe.</span><span class="sxs-lookup"><span data-stu-id="13ec1-108">The **Add-AzureNodeWorkerRole** cmdlet creates the required files and folders, sometimes referred to as scaffolding, for a Node.js application to be hosted in the cloud via node.exe.</span></span>

## <span data-ttu-id="13ec1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13ec1-109">EXAMPLES</span></span>

### <span data-ttu-id="13ec1-110">Przykład 1: rola pracownika pojedynczego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="13ec1-110">Example 1: Single instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole
```

<span data-ttu-id="13ec1-111">W tym przykładzie dodano rusztowania dla jednej roli pracownika o nazwie **MyWorkerRole** do bieżącej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="13ec1-111">This example adds scaffolding for a single worker role named **MyWorkerRole** to the current application.</span></span>

### <span data-ttu-id="13ec1-112">Przykład 2: rola procesu roboczego wielu wystąpień</span><span class="sxs-lookup"><span data-stu-id="13ec1-112">Example 2: Multiple instance worker role</span></span>
```
PS C:\> Add-AzureNodeWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="13ec1-113">W tym przykładzie dodano szkielety dla jednej roli pracownika o nazwie **MyWorkerRole** do bieżącej aplikacji z liczbą wystąpień roli równą 2.</span><span class="sxs-lookup"><span data-stu-id="13ec1-113">This example adds scaffolding for a single worker role named **MyWorkerRole** to the current application, with a role instance count of 2.</span></span>

## <span data-ttu-id="13ec1-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13ec1-114">PARAMETERS</span></span>

### <span data-ttu-id="13ec1-115">-Wystąpienia</span><span class="sxs-lookup"><span data-stu-id="13ec1-115">-Instances</span></span>
<span data-ttu-id="13ec1-116">Określa liczbę wystąpień roli dla tej roli pracownika.</span><span class="sxs-lookup"><span data-stu-id="13ec1-116">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="13ec1-117">Domyślnie jest to 1.</span><span class="sxs-lookup"><span data-stu-id="13ec1-117">Default is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ec1-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="13ec1-118">-Name</span></span>
<span data-ttu-id="13ec1-119">Określa nazwę roli pracownika.</span><span class="sxs-lookup"><span data-stu-id="13ec1-119">Specifies the name of the worker role.</span></span>
<span data-ttu-id="13ec1-120">Wartość określa nazwę folderu, który zawiera rusztowania dla usługi node.js obsługiwanej w roli procesu roboczego.</span><span class="sxs-lookup"><span data-stu-id="13ec1-120">The value determines the folder name that contains the scaffolding for the node.js service hosted in the worker role.</span></span>
<span data-ttu-id="13ec1-121">Domyślna to WorkerRole1.</span><span class="sxs-lookup"><span data-stu-id="13ec1-121">Default is WorkerRole1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ec1-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="13ec1-122">-Profile</span></span>
<span data-ttu-id="13ec1-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13ec1-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="13ec1-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="13ec1-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ec1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13ec1-125">CommonParameters</span></span>
<span data-ttu-id="13ec1-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13ec1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13ec1-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13ec1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13ec1-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13ec1-128">INPUTS</span></span>

## <span data-ttu-id="13ec1-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13ec1-129">OUTPUTS</span></span>

## <span data-ttu-id="13ec1-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13ec1-130">NOTES</span></span>

## <span data-ttu-id="13ec1-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13ec1-131">RELATED LINKS</span></span>

[<span data-ttu-id="13ec1-132">Dodaj-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="13ec1-132">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="13ec1-133">Nowe — AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="13ec1-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


