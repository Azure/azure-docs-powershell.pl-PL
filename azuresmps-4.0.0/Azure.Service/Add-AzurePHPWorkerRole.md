---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FEFBF1EF-FBCE-45D8-8455-F3F8662F1F36
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4ddf78f30cb6938571fc967d510e4ab99a0cfc80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055353"
---
# <span data-ttu-id="23b77-101">Add-AzurePHPWorkerRole</span><span class="sxs-lookup"><span data-stu-id="23b77-101">Add-AzurePHPWorkerRole</span></span>

## <span data-ttu-id="23b77-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23b77-102">SYNOPSIS</span></span>
<span data-ttu-id="23b77-103">Tworzy wymagane pliki i konfigurację dla aplikacji PHP, która będzie hostowana na platformie Azure przez php.exe.</span><span class="sxs-lookup"><span data-stu-id="23b77-103">Creates the required files and configuration for a PHP application that will be hosted in Azure through php.exe.</span></span>

## <span data-ttu-id="23b77-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23b77-104">SYNTAX</span></span>

```
Add-AzurePHPWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="23b77-105">Opis</span><span class="sxs-lookup"><span data-stu-id="23b77-105">DESCRIPTION</span></span>
<span data-ttu-id="23b77-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="23b77-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="23b77-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="23b77-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="23b77-108">Tworzy wymagane pliki i konfigurację, czasami nazywane rusztowami, w aplikacji PHP, która będzie hostowana na platformie Azure przez php.exe.</span><span class="sxs-lookup"><span data-stu-id="23b77-108">Creates the required files and configuration, sometimes referred to as scaffolding, for a PHP application that will be hosted in Azure through php.exe.</span></span>

## <span data-ttu-id="23b77-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23b77-109">EXAMPLES</span></span>

### <span data-ttu-id="23b77-110">Przykład 1. Tworzenie roli pracownika za pomocą jednego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="23b77-110">Example 1: Create a worker role with a single instance</span></span>
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole
```

<span data-ttu-id="23b77-111">W tym przykładzie dodano wymagane pliki i konfigurację dla jednej roli pracownika o nazwie MyWorkerRole do bieżącej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="23b77-111">This example adds the required files and configuration for a single worker role named MyWorkerRole to the current application.</span></span>

### <span data-ttu-id="23b77-112">Przykład 2: tworzenie roli pracownika z wieloma wystąpieniami</span><span class="sxs-lookup"><span data-stu-id="23b77-112">Example 2: Create a worker role with multiple instances</span></span>
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="23b77-113">W tym przykładzie zostaną dodane wymagane pliki i konfiguracja dla nowej roli procesu roboczego w bieżącej aplikacji przy użyciu nazwy MyWorkerRole z liczbą wystąpień roli równą 2.</span><span class="sxs-lookup"><span data-stu-id="23b77-113">This example adds the required files and configuration for a new worker role to the current application, using the name MyWorkerRole with a role instance count of 2.</span></span>

## <span data-ttu-id="23b77-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23b77-114">PARAMETERS</span></span>

### <span data-ttu-id="23b77-115">-Wystąpienia</span><span class="sxs-lookup"><span data-stu-id="23b77-115">-Instances</span></span>
<span data-ttu-id="23b77-116">Określa liczbę wystąpień roli dla tej roli pracownika.</span><span class="sxs-lookup"><span data-stu-id="23b77-116">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="23b77-117">Wartość domyślna to 1.</span><span class="sxs-lookup"><span data-stu-id="23b77-117">The default is 1.</span></span>

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

### <span data-ttu-id="23b77-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="23b77-118">-Name</span></span>
<span data-ttu-id="23b77-119">Określa nazwę roli pracownika.</span><span class="sxs-lookup"><span data-stu-id="23b77-119">Specifies the name of the worker role.</span></span>
<span data-ttu-id="23b77-120">Nazwa Określa nazwę folderu zawierającego wymagane pliki i konfigurację dla usługi PHP obsługiwanej w roli procesu roboczego.</span><span class="sxs-lookup"><span data-stu-id="23b77-120">The name determines the folder name that contains the required files and configuration for the PHP service hosted in the worker role.</span></span>
<span data-ttu-id="23b77-121">Wartość domyślna to WorkerRole1.</span><span class="sxs-lookup"><span data-stu-id="23b77-121">The default is WorkerRole1.</span></span>

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

### <span data-ttu-id="23b77-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="23b77-122">-Profile</span></span>
<span data-ttu-id="23b77-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23b77-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="23b77-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="23b77-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="23b77-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23b77-125">CommonParameters</span></span>
<span data-ttu-id="23b77-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23b77-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23b77-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23b77-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23b77-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23b77-128">INPUTS</span></span>

## <span data-ttu-id="23b77-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23b77-129">OUTPUTS</span></span>

## <span data-ttu-id="23b77-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23b77-130">NOTES</span></span>

## <span data-ttu-id="23b77-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23b77-131">RELATED LINKS</span></span>

[<span data-ttu-id="23b77-132">Nowe — AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="23b77-132">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="23b77-133">Dodaj-AzurePHPWebRole</span><span class="sxs-lookup"><span data-stu-id="23b77-133">Add-AzurePHPWebRole</span></span>](./Add-AzurePHPWebRole.md)


