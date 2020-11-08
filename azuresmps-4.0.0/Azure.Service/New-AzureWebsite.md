---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FBB55071-454D-4473-93BA-D97F33067785
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f83489d21fba97bb50145de1fedc1ac9a7195a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055150"
---
# <span data-ttu-id="dc5df-101">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="dc5df-101">New-AzureWebsite</span></span>

## <span data-ttu-id="dc5df-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dc5df-102">SYNOPSIS</span></span>
<span data-ttu-id="dc5df-103">Utwórz nową witrynę sieci Web do uruchamiania na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="dc5df-103">Create a new website to run in Azure.</span></span>

## <span data-ttu-id="dc5df-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dc5df-104">SYNTAX</span></span>

```
New-AzureWebsite [-Location <String>] [-Hostname <String>] [-PublishingUsername <String>] [-Git] [-GitHub]
 [-GithubCredentials <PSCredential>] [-GithubRepository <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dc5df-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dc5df-105">DESCRIPTION</span></span>
<span data-ttu-id="dc5df-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="dc5df-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="dc5df-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="dc5df-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="dc5df-108">Polecenie cmdlet tworzy nową witrynę sieci Web do uruchamiania na platformie Azure i przygotowywanie jej do wdrożenia za pośrednictwem usługi GitHub.</span><span class="sxs-lookup"><span data-stu-id="dc5df-108">The cmdlet creates a new website to run in Azure and prepares for deployment through Github.</span></span>

## <span data-ttu-id="dc5df-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dc5df-109">EXAMPLES</span></span>

### <span data-ttu-id="dc5df-110">Przykład 1. Tworzenie nowej witryny sieci Web przy użyciu narzędzia Git</span><span class="sxs-lookup"><span data-stu-id="dc5df-110">Example 1: Create a new website with Git</span></span>
```
PS C:\> New-AzureWebsite mySite -Git
```

<span data-ttu-id="dc5df-111">W tym przykładzie jest tworzona nowa witryna sieci Web na platformie Azure oraz lokalne repozytorium git używane do wdrażania plików w nowej witrynie sieci Web.</span><span class="sxs-lookup"><span data-stu-id="dc5df-111">This example creates a new website in Azure and a local Git repository to use for deploying files to the new website.</span></span>

### <span data-ttu-id="dc5df-112">Przykład 2: Tworzenie witryny sieci Web zintegrowanej z usługą GitHub</span><span class="sxs-lookup"><span data-stu-id="dc5df-112">Example 2: Create website integrated with Github</span></span>
```
PS C:\> New-AzureWebsite mysite -Github -GithubRepository myaccount/myrepo
```

<span data-ttu-id="dc5df-113">W tym przykładzie jest tworzona nowa witryna sieci Web połączona z repozytorium GitHub o nazwie Moje konto/moje repozytorium.</span><span class="sxs-lookup"><span data-stu-id="dc5df-113">This example creates a new website linked to a Github repository named myaccount/myrepo.</span></span>
<span data-ttu-id="dc5df-114">Zatwierdzanie repozytorium GitHub jest przekazywane do witryny sieci Web na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="dc5df-114">Commits to the Github repository are pushed to the website in Azure.</span></span>

## <span data-ttu-id="dc5df-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dc5df-115">PARAMETERS</span></span>

### <span data-ttu-id="dc5df-116">-Git</span><span class="sxs-lookup"><span data-stu-id="dc5df-116">-Git</span></span>
<span data-ttu-id="dc5df-117">Konfiguruje lokalne repozytorium git i łączy je z witryną internetową.</span><span class="sxs-lookup"><span data-stu-id="dc5df-117">Sets up a local Git repository and links it to the website.</span></span>
<span data-ttu-id="dc5df-118">W przypadku określenia tego parametru ten parametr konfiguruje repozytorium Git w katalogu lokalnym i dodanie repozytorium zdalnego o nazwie "Azure" połączonego z witryną internetową na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="dc5df-118">If specified, this parameter sets up a Git repository in the local directory and add a remote repository named 'azure' that links to the website in Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc5df-119">-GitHub</span><span class="sxs-lookup"><span data-stu-id="dc5df-119">-GitHub</span></span>
<span data-ttu-id="dc5df-120">Wskazuje, że to polecenie cmdlet łączy nową witrynę sieci Web z istniejącym repozytorium GitHub.</span><span class="sxs-lookup"><span data-stu-id="dc5df-120">Indicates that this cmdlet links the new website to an existing Github repository.</span></span>
<span data-ttu-id="dc5df-121">Zatwierdzanie repozytorium Giuthub jest przekazywane do witryny sieci Web na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="dc5df-121">Commits to the Giuthub repository are pushed to the website in Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc5df-122">-GithubCredentials</span><span class="sxs-lookup"><span data-stu-id="dc5df-122">-GithubCredentials</span></span>
<span data-ttu-id="dc5df-123">Określa poświadczenia nazwy użytkownika i hasła w celu nawiązania połączenia z usługą GitHub.</span><span class="sxs-lookup"><span data-stu-id="dc5df-123">Specifies the user name and password credentials to connect to Github.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc5df-124">-GithubRepository</span><span class="sxs-lookup"><span data-stu-id="dc5df-124">-GithubRepository</span></span>
<span data-ttu-id="dc5df-125">Określa pełną nazwę repozytorium GitHub, które ma zostać połączone z tą witryną internetową.</span><span class="sxs-lookup"><span data-stu-id="dc5df-125">Specifies the full name of the Github repository to link to this website.</span></span>
<span data-ttu-id="dc5df-126">Na przykład `myaccount/myrepo` .</span><span class="sxs-lookup"><span data-stu-id="dc5df-126">For example, `myaccount/myrepo`.</span></span>

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

### <span data-ttu-id="dc5df-127">-Hostname</span><span class="sxs-lookup"><span data-stu-id="dc5df-127">-Hostname</span></span>
<span data-ttu-id="dc5df-128">Określa alternatywną nazwę hosta dla nowej witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="dc5df-128">Specifies an alternative host name for the new website.</span></span>

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

### <span data-ttu-id="dc5df-129">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="dc5df-129">-Location</span></span>
<span data-ttu-id="dc5df-130">Określa lokalizację centrum danych, w którym ma zostać wdrożona witryna sieci Web.</span><span class="sxs-lookup"><span data-stu-id="dc5df-130">Specifies the location of the data center where you want to deploy the website.</span></span>

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

### <span data-ttu-id="dc5df-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dc5df-131">-Name</span></span>
<span data-ttu-id="dc5df-132">Określa nazwę witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="dc5df-132">Specifies a name for the website.</span></span>

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

### <span data-ttu-id="dc5df-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="dc5df-133">-Profile</span></span>
<span data-ttu-id="dc5df-134">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc5df-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dc5df-135">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="dc5df-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dc5df-136">-PublishingUsername</span><span class="sxs-lookup"><span data-stu-id="dc5df-136">-PublishingUsername</span></span>
<span data-ttu-id="dc5df-137">Określa nazwę użytkownika określoną w portalu Azure dla wdrożenia git.</span><span class="sxs-lookup"><span data-stu-id="dc5df-137">Specifies the user name you have specified in the Azure Portal for Git deployment.</span></span>

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

### <span data-ttu-id="dc5df-138">-Slot</span><span class="sxs-lookup"><span data-stu-id="dc5df-138">-Slot</span></span>
<span data-ttu-id="dc5df-139">Określa nazwę gniazda witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="dc5df-139">Specifies a slot name for the website.</span></span>

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

### <span data-ttu-id="dc5df-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc5df-140">CommonParameters</span></span>
<span data-ttu-id="dc5df-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc5df-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc5df-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc5df-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc5df-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc5df-143">INPUTS</span></span>

## <span data-ttu-id="dc5df-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dc5df-144">OUTPUTS</span></span>

## <span data-ttu-id="dc5df-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dc5df-145">NOTES</span></span>

## <span data-ttu-id="dc5df-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc5df-146">RELATED LINKS</span></span>

[<span data-ttu-id="dc5df-147">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="dc5df-147">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


