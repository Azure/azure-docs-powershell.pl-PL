---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FB5CD696-108D-4A3E-8983-1C6562E8795A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25ade8ccf395d37ab0856742fe473a6508c9d63b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054677"
---
# <span data-ttu-id="b3221-101">Add-AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="b3221-101">Add-AzureWebRole</span></span>

## <span data-ttu-id="b3221-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b3221-102">SYNOPSIS</span></span>
<span data-ttu-id="b3221-103">Dodaje rolę pracownika sieci Web.</span><span class="sxs-lookup"><span data-stu-id="b3221-103">Adds a web worker role.</span></span>

## <span data-ttu-id="b3221-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b3221-104">SYNTAX</span></span>

```
Add-AzureWebRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3221-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b3221-105">DESCRIPTION</span></span>
<span data-ttu-id="b3221-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b3221-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b3221-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b3221-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b3221-108">Polecenie cmdlet **Add-AzureWebRole** umożliwia dodanie roli pracownika sieci Web.</span><span class="sxs-lookup"><span data-stu-id="b3221-108">The **Add-AzureWebRole** cmdlet adds a web worker role.</span></span>

## <span data-ttu-id="b3221-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b3221-109">EXAMPLES</span></span>

### <span data-ttu-id="b3221-110">Przykład 1. Dodaj domyślną rolę</span><span class="sxs-lookup"><span data-stu-id="b3221-110">Example 1: Add a default role</span></span>
```
PS C:\> Add-AzureWebRole
```

<span data-ttu-id="b3221-111">To polecenie dodaje rolę sieci Web, która ma domyślną konfigurację Webrole1 jako nazwę i jedno wystąpienie.</span><span class="sxs-lookup"><span data-stu-id="b3221-111">This command add web role that has the default configuration of Webrole1 as the name and a single instance.</span></span>

### <span data-ttu-id="b3221-112">Przykład 2: Dodawanie roli o nazwie</span><span class="sxs-lookup"><span data-stu-id="b3221-112">Example 2: Add a role with a name</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole"
```

<span data-ttu-id="b3221-113">To polecenie dodaje pojedynczą rolę sieci Web o nazwie MyWebRole do bieżącej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b3221-113">This command adds a single web role named MyWebRole to the current application.</span></span>

### <span data-ttu-id="b3221-114">Przykład 3: Dodawanie roli z nazwą i liczbą wystąpień</span><span class="sxs-lookup"><span data-stu-id="b3221-114">Example 3: Add a role with a name and instance count</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -Instance 2
```

<span data-ttu-id="b3221-115">To polecenie dodaje rolę sieci Web o nazwie MyWebRole do bieżącej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b3221-115">This command adds a web role named MyWebRole to the current application.</span></span>
<span data-ttu-id="b3221-116">Polecenie cmdlet ma liczbę wystąpień roli 2.</span><span class="sxs-lookup"><span data-stu-id="b3221-116">The cmdlet has a role instance count of 2.</span></span>

### <span data-ttu-id="b3221-117">Przykład 4: Dodawanie roli o nazwie i szablonie</span><span class="sxs-lookup"><span data-stu-id="b3221-117">Example 4: Add a role with a name and template</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -TemplateFolder ".\MyWebTemplateFolder"
```

<span data-ttu-id="b3221-118">To polecenie dodaje pojedynczą rolę sieci Web o nazwie MyWebRole do bieżącej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b3221-118">This command adds a single web role named MyWebRole to the current application.</span></span>
<span data-ttu-id="b3221-119">Polecenie określa folder o nazwie MyWebTemplateFolder jako szablon szkieletu.</span><span class="sxs-lookup"><span data-stu-id="b3221-119">The command specifies a folder named MyWebTemplateFolder as a scaffolding template.</span></span>

## <span data-ttu-id="b3221-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b3221-120">PARAMETERS</span></span>

### <span data-ttu-id="b3221-121">-Wystąpienia</span><span class="sxs-lookup"><span data-stu-id="b3221-121">-Instances</span></span>
<span data-ttu-id="b3221-122">Określa liczbę wystąpień.</span><span class="sxs-lookup"><span data-stu-id="b3221-122">Specifies the number of instances.</span></span>

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

### <span data-ttu-id="b3221-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b3221-123">-Name</span></span>
<span data-ttu-id="b3221-124">Określa nazwę roli sieci Web.</span><span class="sxs-lookup"><span data-stu-id="b3221-124">Specifies the name of the web role.</span></span>

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

### <span data-ttu-id="b3221-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="b3221-125">-Profile</span></span>
<span data-ttu-id="b3221-126">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3221-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b3221-127">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="b3221-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b3221-128">-TemplateFolder</span><span class="sxs-lookup"><span data-stu-id="b3221-128">-TemplateFolder</span></span>
<span data-ttu-id="b3221-129">Określa folder szablonów.</span><span class="sxs-lookup"><span data-stu-id="b3221-129">Specifies the template folder.</span></span>

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

### <span data-ttu-id="b3221-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3221-130">CommonParameters</span></span>
<span data-ttu-id="b3221-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3221-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3221-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3221-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3221-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3221-133">INPUTS</span></span>

## <span data-ttu-id="b3221-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b3221-134">OUTPUTS</span></span>

## <span data-ttu-id="b3221-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b3221-135">NOTES</span></span>

## <span data-ttu-id="b3221-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3221-136">RELATED LINKS</span></span>

[<span data-ttu-id="b3221-137">Dodaj-AzureWorkerRole</span><span class="sxs-lookup"><span data-stu-id="b3221-137">Add-AzureWorkerRole</span></span>](./Add-AzureWorkerRole.md)

[<span data-ttu-id="b3221-138">Nowe — AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="b3221-138">New-AzureRoleTemplate</span></span>](./New-AzureRoleTemplate.md)


