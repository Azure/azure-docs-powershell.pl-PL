---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C2DAFB2C-A58B-406C-8349-8728771B279E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59aef29c27d7eb96834d270c2fce48ff3acb9554
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055358"
---
# <span data-ttu-id="ea9e9-101">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="ea9e9-101">Add-AzureNodeWebRole</span></span>

## <span data-ttu-id="ea9e9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea9e9-102">SYNOPSIS</span></span>
<span data-ttu-id="ea9e9-103">Tworzy wymagane pliki i foldery dla aplikacji Node.js.</span><span class="sxs-lookup"><span data-stu-id="ea9e9-103">Creates required files and folders for a Node.js application.</span></span>

## <span data-ttu-id="ea9e9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea9e9-104">SYNTAX</span></span>

```
Add-AzureNodeWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ea9e9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ea9e9-105">DESCRIPTION</span></span>
<span data-ttu-id="ea9e9-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ea9e9-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ea9e9-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ea9e9-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ea9e9-108">W **dodatku Add-AzureNodeWebRole** są tworzone wymagane pliki i foldery, czasami nazywane rusztowaniem, aby aplikacja Node.js była hostowana w chmurze za pośrednictwem usług IIS.</span><span class="sxs-lookup"><span data-stu-id="ea9e9-108">The **Add-AzureNodeWebRole** creates required files and folders, sometimes referred to as scaffolding, for a Node.js application to be hosted in the cloud via IIS.</span></span>

## <span data-ttu-id="ea9e9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea9e9-109">EXAMPLES</span></span>

### <span data-ttu-id="ea9e9-110">Przykład 1: rola sieci Web pojedynczego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="ea9e9-110">Example 1: Single instance web role</span></span>
```
PS C:\> Add-AzureNodeWebRole -Name MyWebRole
```

<span data-ttu-id="ea9e9-111">W tym przykładzie dodano rusztowania dla jednej roli sieci Web o nazwie **MyWebRole** do bieżącej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ea9e9-111">This example adds scaffolding for a single web role named **MyWebRole** to the current application.</span></span>

### <span data-ttu-id="ea9e9-112">Przykład 2: rola sieci Web o wielu wystąpieniach</span><span class="sxs-lookup"><span data-stu-id="ea9e9-112">Example 2: Multiple instance web role</span></span>
```
PS C:\> Add-AzureNodeWebRole MyWebRole -I 2
```

<span data-ttu-id="ea9e9-113">W tym przykładzie dodano rusztowania dla nowej roli sieci Web o nazwie **MyWebRole** do bieżącej aplikacji z liczbą wystąpień roli równą 2.</span><span class="sxs-lookup"><span data-stu-id="ea9e9-113">This example adds scaffolding for a new web role named **MyWebRole** to the current application, with a role instance count of 2.</span></span>

## <span data-ttu-id="ea9e9-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea9e9-114">PARAMETERS</span></span>

### <span data-ttu-id="ea9e9-115">-Wystąpienia</span><span class="sxs-lookup"><span data-stu-id="ea9e9-115">-Instances</span></span>
<span data-ttu-id="ea9e9-116">Określa liczbę wystąpień roli dla tej roli sieci Web.</span><span class="sxs-lookup"><span data-stu-id="ea9e9-116">Specifies the number of role instances for this web role.</span></span>
<span data-ttu-id="ea9e9-117">Wartość domyślna to 1.</span><span class="sxs-lookup"><span data-stu-id="ea9e9-117">The default is 1.</span></span>

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

### <span data-ttu-id="ea9e9-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ea9e9-118">-Name</span></span>
<span data-ttu-id="ea9e9-119">Określa nazwę roli sieci Web.</span><span class="sxs-lookup"><span data-stu-id="ea9e9-119">Specifies the name of the web role.</span></span>
<span data-ttu-id="ea9e9-120">Określa również nazwę katalogu zawierającego rusztowania dla aplikacji node.js, która będzie hostowana w roli sieci Web.</span><span class="sxs-lookup"><span data-stu-id="ea9e9-120">It also determines the name of the directory that contains the scaffolding for the node.js application that will be hosted in the web role.</span></span>
<span data-ttu-id="ea9e9-121">Wartość domyślna to webrola #, gdzie # wskazuje liczbę ról sieci Web w usłudze.</span><span class="sxs-lookup"><span data-stu-id="ea9e9-121">The default is WebRole#, where # indicates the number of web roles in the service.</span></span>

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

### <span data-ttu-id="ea9e9-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="ea9e9-122">-Profile</span></span>
<span data-ttu-id="ea9e9-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea9e9-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ea9e9-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="ea9e9-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ea9e9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea9e9-125">CommonParameters</span></span>
<span data-ttu-id="ea9e9-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea9e9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea9e9-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea9e9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea9e9-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea9e9-128">INPUTS</span></span>

## <span data-ttu-id="ea9e9-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea9e9-129">OUTPUTS</span></span>

## <span data-ttu-id="ea9e9-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea9e9-130">NOTES</span></span>

## <span data-ttu-id="ea9e9-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea9e9-131">RELATED LINKS</span></span>

[<span data-ttu-id="ea9e9-132">Dodaj-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="ea9e9-132">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="ea9e9-133">Nowe — AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="ea9e9-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


