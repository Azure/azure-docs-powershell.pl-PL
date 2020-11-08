---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F9A06B8B-55DB-48A5-B246-53347E759E64
online version: ''
schema: 2.0.0
ms.openlocfilehash: 050c05f2cdad546388744bcebca4f28a12a03038
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055356"
---
# <span data-ttu-id="9858c-101">Add-AzurePHPWebRole</span><span class="sxs-lookup"><span data-stu-id="9858c-101">Add-AzurePHPWebRole</span></span>

## <span data-ttu-id="9858c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9858c-102">SYNOPSIS</span></span>
<span data-ttu-id="9858c-103">Tworzy wymagane pliki i konfigurację dla aplikacji PHP.</span><span class="sxs-lookup"><span data-stu-id="9858c-103">Creates the required files and configuration for a PHP application.</span></span>

## <span data-ttu-id="9858c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9858c-104">SYNTAX</span></span>

```
Add-AzurePHPWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9858c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9858c-105">DESCRIPTION</span></span>
<span data-ttu-id="9858c-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9858c-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9858c-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="9858c-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="9858c-108">Polecenie cmdlet **Add-AzurePHPWebRole** tworzy pliki i konfigurację, czasami nazywane rusztowaniem, dla aplikacji PHP, która będzie hostowana na platformie Azure za pośrednictwem internetowych usług informacyjnych.</span><span class="sxs-lookup"><span data-stu-id="9858c-108">The **Add-AzurePHPWebRole** cmdlet creates the files and configuration, sometimes referred to as scaffolding, for a PHP application that will be hosted in Azure through IIS.</span></span>

## <span data-ttu-id="9858c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9858c-109">EXAMPLES</span></span>

### <span data-ttu-id="9858c-110">Przykład 1: Dodawanie roli w sieci Web przy użyciu wartości domyślnych</span><span class="sxs-lookup"><span data-stu-id="9858c-110">Example 1: Add a web role using default values</span></span>
```
PS C:\> Add-AzurePHPWebRole
```

<span data-ttu-id="9858c-111">W tym przykładzie dodano wymagane pliki i konfigurację dla nowej roli w sieci Web przy użyciu wartości domyślnych usługi o nazwie "WebRole1" z jedną instancją.</span><span class="sxs-lookup"><span data-stu-id="9858c-111">This example adds the required files and configuration for new web role using the default values of a service named "WebRole1" with 1 instance.</span></span>

### <span data-ttu-id="9858c-112">Przykład 2: Dodawanie roli sieci Web z wieloma wystąpieniami</span><span class="sxs-lookup"><span data-stu-id="9858c-112">Example 2: Add a web role with multiple instances</span></span>
```
PS C:\> Add-AzurePHPWebRole MyWebRole -I 2
```

<span data-ttu-id="9858c-113">W tym przykładzie zostaną dodane wymagane pliki i konfiguracja nowej roli sieci Web w bieżącej aplikacji przy użyciu nazwy "MyWebRole" i liczby wystąpień roli 2.</span><span class="sxs-lookup"><span data-stu-id="9858c-113">This example adds the required files and configuration for a new web role to the current application, using the name "MyWebRole" and a role instance count of 2.</span></span>

## <span data-ttu-id="9858c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9858c-114">PARAMETERS</span></span>

### <span data-ttu-id="9858c-115">-Wystąpienia</span><span class="sxs-lookup"><span data-stu-id="9858c-115">-Instances</span></span>
<span data-ttu-id="9858c-116">Określa liczbę wystąpień roli dla tej roli sieci Web.</span><span class="sxs-lookup"><span data-stu-id="9858c-116">Specifies the number of role instances for this web role.</span></span>
<span data-ttu-id="9858c-117">Wartość domyślna to 1.</span><span class="sxs-lookup"><span data-stu-id="9858c-117">The default is 1.</span></span>

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

### <span data-ttu-id="9858c-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9858c-118">-Name</span></span>
<span data-ttu-id="9858c-119">Określa nazwę roli sieci Web.</span><span class="sxs-lookup"><span data-stu-id="9858c-119">Specifies the name of the web role.</span></span>
<span data-ttu-id="9858c-120">Nazwa Określa nazwę katalogu zawierającego wymagane pliki i konfigurację dla aplikacji PHP.</span><span class="sxs-lookup"><span data-stu-id="9858c-120">The name determines the name of the directory that contains the required files and configuration for the PHP application.</span></span>
<span data-ttu-id="9858c-121">Wartość domyślna to webrola #, gdzie # to liczba ról sieci Web w usłudze.</span><span class="sxs-lookup"><span data-stu-id="9858c-121">The default is WebRole#, where # is the number of web roles in the service.</span></span>

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

### <span data-ttu-id="9858c-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="9858c-122">-Profile</span></span>
<span data-ttu-id="9858c-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9858c-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9858c-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="9858c-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9858c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9858c-125">CommonParameters</span></span>
<span data-ttu-id="9858c-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9858c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9858c-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9858c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9858c-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9858c-128">INPUTS</span></span>

## <span data-ttu-id="9858c-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9858c-129">OUTPUTS</span></span>

## <span data-ttu-id="9858c-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9858c-130">NOTES</span></span>

## <span data-ttu-id="9858c-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9858c-131">RELATED LINKS</span></span>

[<span data-ttu-id="9858c-132">Dodaj-AzurePHPWorkerRole</span><span class="sxs-lookup"><span data-stu-id="9858c-132">Add-AzurePHPWorkerRole</span></span>](./Add-AzurePHPWorkerRole.md)

[<span data-ttu-id="9858c-133">Nowe — AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="9858c-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


