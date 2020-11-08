---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3B3F1870-348D-4303-9520-FD81D4650F5F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2103a155b12fdf1e481173d529ff3308a3b2200b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055478"
---
# <span data-ttu-id="d5c14-101">Get-AzureWebHostingPlan</span><span class="sxs-lookup"><span data-stu-id="d5c14-101">Get-AzureWebHostingPlan</span></span>

## <span data-ttu-id="d5c14-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d5c14-102">SYNOPSIS</span></span>
<span data-ttu-id="d5c14-103">Pobiera plany hostingu usługi Azure w sieci Web w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d5c14-103">Gets Azure web hosting plans in the current subscription.</span></span>

## <span data-ttu-id="d5c14-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d5c14-104">SYNTAX</span></span>

```
Get-AzureWebHostingPlan [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5c14-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d5c14-105">DESCRIPTION</span></span>
<span data-ttu-id="d5c14-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d5c14-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d5c14-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="d5c14-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d5c14-108">Polecenie cmdlet **Get-AzureWebHostingPlan** pobiera plany hostingu w sieci Azure w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d5c14-108">The **Get-AzureWebHostingPlan** cmdlet gets the Azure web hosting plans in the current subscription.</span></span>

<span data-ttu-id="d5c14-109">Domyślnie funkcja **Get-AzureWebHostingPlan** pobiera wszystkie plany hostingu platformy Azure w bieżącej subskrypcji i zwraca obiekt, który dostarcza podstawowych informacji o planach.</span><span class="sxs-lookup"><span data-stu-id="d5c14-109">By default, **Get-AzureWebHostingPlan** gets all Azure hosting plans in the current subscription and returns an object that provides basic information about the plans.</span></span>
<span data-ttu-id="d5c14-110">Gdy korzystasz z parametrów *przestrzeni* sieci i *nazwy* , funkcja **Get-AzureWebHostingPlan** zwraca konkretny obiekt planu hostingu.</span><span class="sxs-lookup"><span data-stu-id="d5c14-110">When you use the *WebSpace* and *Name* parameters, **Get-AzureWebHostingPlan** returns a specific hosting plan object.</span></span>

<span data-ttu-id="d5c14-111">Aby znaleźć bieżącą subskrypcję, użyj *bieżącego* parametru polecenia cmdlet **Get-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="d5c14-111">To find the current subscription, use the *Current* parameter of the **Get-AzureSubscription** cmdlet.</span></span>
<span data-ttu-id="d5c14-112">Aby zmienić bieżącą subskrypcję, użyj polecenia cmdlet **SELECT-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="d5c14-112">To change the current subscription, use the **Select-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="d5c14-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d5c14-113">EXAMPLES</span></span>

### <span data-ttu-id="d5c14-114">Przykład 1: pobieranie wszystkich planów hostingu w sieci Web w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d5c14-114">Example 1: Get all web hosting plans in a subscription</span></span>
```
PS C:\> Get-AzureWebHostingPlan 

Name : Default1 
SKU : Basic 
WorkerSize : Small 
NumberOfWorkers : 1 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 1 
Status : Ready 
WebSpace : eastuswebspace 
Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready
```

<span data-ttu-id="d5c14-115">To polecenie pobiera wszystkie plany hostingu w sieci Web w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d5c14-115">This command gets all Azure web hosting plans in the current subscription.</span></span>

### <span data-ttu-id="d5c14-116">Przykład 2: uzyskiwanie określonego planu hostingu w witrynie sieci Web w ramach abonamentu</span><span class="sxs-lookup"><span data-stu-id="d5c14-116">Example 2: Get a specific web hosting plan in a subscription</span></span>
```
PS C:\> Get-AzureWebHostingPlan -WebSpaceName "westeuropewebspace" -Name "Default0" 

Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready 
WebSpace : westeuropewebspace
```

<span data-ttu-id="d5c14-117">To polecenie pobiera plan hostingu w sieci Web o nazwie Default0 w obszarze webspace o nazwie westeuropewebspace w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d5c14-117">This command gets the web hosting plan named Default0 in the webspace named westeuropewebspace in the current subscription.</span></span>

## <span data-ttu-id="d5c14-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d5c14-118">PARAMETERS</span></span>

### <span data-ttu-id="d5c14-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d5c14-119">-Name</span></span>
<span data-ttu-id="d5c14-120">Określa nazwę planu w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d5c14-120">Specifies the name of a plan in the subscription.</span></span>
<span data-ttu-id="d5c14-121">Domyślnie to polecenie cmdlet pobiera wszystkie plany w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d5c14-121">By default, this cmdlet gets all plans in the current subscription.</span></span>
<span data-ttu-id="d5c14-122">Ten parametr nie obsługuje symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="d5c14-122">This parameter does not support wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5c14-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="d5c14-123">-Profile</span></span>
<span data-ttu-id="d5c14-124">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5c14-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d5c14-125">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="d5c14-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d5c14-126">-Webspacename</span><span class="sxs-lookup"><span data-stu-id="d5c14-126">-WebSpaceName</span></span>
<span data-ttu-id="d5c14-127">Określa nazwę przestrzeni sieci w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d5c14-127">Specifies the name of a webspace in the subscription.</span></span>
<span data-ttu-id="d5c14-128">Domyślnie to polecenie cmdlet umożliwia pobieranie wszystkich witryn internetowych w określonym obszarze sieci Web.</span><span class="sxs-lookup"><span data-stu-id="d5c14-128">By default, this cmdlet gets all websites in the specified webspace.</span></span>
<span data-ttu-id="d5c14-129">Ten parametr nie obsługuje symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="d5c14-129">This parameter does not support wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5c14-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5c14-130">CommonParameters</span></span>
<span data-ttu-id="d5c14-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5c14-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5c14-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5c14-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5c14-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5c14-133">INPUTS</span></span>

###  
<span data-ttu-id="d5c14-134">Do tego polecenia cmdlet można przekazać dane wejściowe według nazwy właściwości, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="d5c14-134">You can pass input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="d5c14-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d5c14-135">OUTPUTS</span></span>

### <span data-ttu-id="d5c14-136">Microsoft. platformy windowsazure. Commands. Utilities. Web. Services. webentities. WebHostingPlan</span><span class="sxs-lookup"><span data-stu-id="d5c14-136">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.WebHostingPlan</span></span>
<span data-ttu-id="d5c14-137">Domyślnie funkcja **Get-AzureWebHostingPlan** zwraca tablicę obiektów **WebHostingPlan** .</span><span class="sxs-lookup"><span data-stu-id="d5c14-137">By default, **Get-AzureWebHostingPlan** returns an array of **WebHostingPlan** objects.</span></span>

## <span data-ttu-id="d5c14-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d5c14-138">NOTES</span></span>

## <span data-ttu-id="d5c14-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5c14-139">RELATED LINKS</span></span>

