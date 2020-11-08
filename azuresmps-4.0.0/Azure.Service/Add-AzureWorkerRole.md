---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8632A865-D4CC-4AE5-8307-055CDD776D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b79ee50bb5097896c2a120a9b7316adb2146b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054676"
---
# <span data-ttu-id="c2b14-101">Add-AzureWorkerRole</span><span class="sxs-lookup"><span data-stu-id="c2b14-101">Add-AzureWorkerRole</span></span>

## <span data-ttu-id="c2b14-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2b14-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b14-103">Tworzy wymagane pliki i konfigurację dla niestandardowej roli pracownika.</span><span class="sxs-lookup"><span data-stu-id="c2b14-103">Creates required files and configuration for a custom worker role.</span></span>

## <span data-ttu-id="c2b14-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2b14-104">SYNTAX</span></span>

```
Add-AzureWorkerRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c2b14-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c2b14-105">DESCRIPTION</span></span>
<span data-ttu-id="c2b14-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c2b14-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c2b14-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="c2b14-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c2b14-108">Polecenie cmdlet **Add-AzureWorkerRole** tworzy wymagane pliki i konfigurację, czasami nazywane rusztowaniem, dla niestandardowej roli pracownika.</span><span class="sxs-lookup"><span data-stu-id="c2b14-108">The **Add-AzureWorkerRole** cmdlet creates required files and configuration, sometimes referred to as scaffolding, for a custom worker role.</span></span>

## <span data-ttu-id="c2b14-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2b14-109">EXAMPLES</span></span>

### <span data-ttu-id="c2b14-110">Przykład 1. Tworzenie roli pracownika jednego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="c2b14-110">Example 1: Create a single instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole -Name MyWorkerRole
```

<span data-ttu-id="c2b14-111">W tym przykładzie dodano rusztowania dla jednej roli pracownika o nazwie MyWorkerRole do bieżącej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c2b14-111">This example adds scaffolding for a single worker role named MyWorkerRole to the current application.</span></span>

### <span data-ttu-id="c2b14-112">Przykład 2: tworzenie roli pracownika wielu wystąpień</span><span class="sxs-lookup"><span data-stu-id="c2b14-112">Example 2: Create a multiple instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="c2b14-113">W tym przykładzie dodano rusztowania dla nowej roli pracownika o nazwie MyWorkerRole do bieżącej aplikacji z liczbą wystąpień roli równą 2.</span><span class="sxs-lookup"><span data-stu-id="c2b14-113">This example adds scaffolding for a new worker role named MyWorkerRole to the current application, with a role instance count of 2.</span></span>

### <span data-ttu-id="c2b14-114">Przykład 3: tworzenie roli pracownika przy użyciu szkieletu niestandardowego</span><span class="sxs-lookup"><span data-stu-id="c2b14-114">Example 3: Create worker role with custom scaffolding</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -TemplateFoldr .\MyWorkerRoleTemplate
```

<span data-ttu-id="c2b14-115">W tym przykładzie jest tworzona rola pracownika z niestandardową rusztowaniem.</span><span class="sxs-lookup"><span data-stu-id="c2b14-115">This example creates a worker role with custom scaffolding.</span></span>

## <span data-ttu-id="c2b14-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2b14-116">PARAMETERS</span></span>

### <span data-ttu-id="c2b14-117">-Wystąpienia</span><span class="sxs-lookup"><span data-stu-id="c2b14-117">-Instances</span></span>
<span data-ttu-id="c2b14-118">Określa liczbę wystąpień roli dla tej roli pracownika.</span><span class="sxs-lookup"><span data-stu-id="c2b14-118">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="c2b14-119">Wartość domyślna to 1.</span><span class="sxs-lookup"><span data-stu-id="c2b14-119">The default is 1.</span></span>

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

### <span data-ttu-id="c2b14-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c2b14-120">-Name</span></span>
<span data-ttu-id="c2b14-121">Określa nazwę roli pracownika.</span><span class="sxs-lookup"><span data-stu-id="c2b14-121">Specifies the name of the worker role.</span></span>
<span data-ttu-id="c2b14-122">Ta wartość określa nazwę folderu, który zawiera rusztowania dla aplikacji niestandardowej, która będzie obsługiwana w roli pracownika.</span><span class="sxs-lookup"><span data-stu-id="c2b14-122">This value determines the folder name that contains the scaffolding for the custom application that will be hosted in the worker role.</span></span>
<span data-ttu-id="c2b14-123">Wartość domyślna to WorkerRolenumber, gdzie liczba jest liczbą ról procesu roboczego w usłudze.</span><span class="sxs-lookup"><span data-stu-id="c2b14-123">The default is WorkerRolenumber, where number is the number of worker roles in the service.</span></span>

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

### <span data-ttu-id="c2b14-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="c2b14-124">-Profile</span></span>
<span data-ttu-id="c2b14-125">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2b14-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c2b14-126">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="c2b14-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c2b14-127">-TemplateFolder</span><span class="sxs-lookup"><span data-stu-id="c2b14-127">-TemplateFolder</span></span>
<span data-ttu-id="c2b14-128">Określa folder szablonu rusztowania, który ma być wykorzystywany do tworzenia roli pracownika.</span><span class="sxs-lookup"><span data-stu-id="c2b14-128">Specifies the scaffolding template folder to be used to create the worker role.</span></span>

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

### <span data-ttu-id="c2b14-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b14-129">CommonParameters</span></span>
<span data-ttu-id="c2b14-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2b14-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b14-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2b14-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b14-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2b14-132">INPUTS</span></span>

## <span data-ttu-id="c2b14-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2b14-133">OUTPUTS</span></span>

## <span data-ttu-id="c2b14-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2b14-134">NOTES</span></span>

## <span data-ttu-id="c2b14-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2b14-135">RELATED LINKS</span></span>

[<span data-ttu-id="c2b14-136">Dodaj-AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="c2b14-136">Add-AzureWebRole</span></span>](./Add-AzureWebRole.md)

[<span data-ttu-id="c2b14-137">Nowe — AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="c2b14-137">New-AzureRoleTemplate</span></span>](./New-AzureRoleTemplate.md)


