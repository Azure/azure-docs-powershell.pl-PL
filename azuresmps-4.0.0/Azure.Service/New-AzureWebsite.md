---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FBB55071-454D-4473-93BA-D97F33067785
online version: ''
schema: 2.0.0
ms.openlocfilehash: 768eff2dda32c6dfa0bad14f028338d3c5fa1abd
ms.sourcegitcommit: 87730c7ea4f98f628d3fe1b40aa4a9d2885e1c75
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/12/2021
ms.locfileid: "98110482"
---
# <span data-ttu-id="10048-101">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="10048-101">New-AzureWebsite</span></span>

## <span data-ttu-id="10048-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="10048-102">SYNOPSIS</span></span>
<span data-ttu-id="10048-103">Utwórz nową witrynę sieci Web do uruchamiania na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="10048-103">Create a new website to run in Azure.</span></span>

## <span data-ttu-id="10048-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="10048-104">SYNTAX</span></span>

```
New-AzureWebsite [-Location <String>] [-Hostname <String>] [-PublishingUsername <String>] [-Git] [-GitHub]
 [-GitHubCredentials <PSCredential>] [-GitHubRepository <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="10048-105">Opis</span><span class="sxs-lookup"><span data-stu-id="10048-105">DESCRIPTION</span></span>
<span data-ttu-id="10048-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="10048-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="10048-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="10048-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="10048-108">Polecenie cmdlet tworzy nową witrynę sieci Web do uruchamiania na platformie Azure i przygotowywanie jej do wdrożenia za pośrednictwem usługi GitHub.</span><span class="sxs-lookup"><span data-stu-id="10048-108">The cmdlet creates a new website to run in Azure and prepares for deployment through GitHub.</span></span>

## <span data-ttu-id="10048-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="10048-109">EXAMPLES</span></span>

### <span data-ttu-id="10048-110">Przykład 1. Tworzenie nowej witryny sieci Web przy użyciu narzędzia Git</span><span class="sxs-lookup"><span data-stu-id="10048-110">Example 1: Create a new website with Git</span></span>
```
PS C:\> New-AzureWebsite mySite -Git
```

<span data-ttu-id="10048-111">W tym przykładzie jest tworzona nowa witryna sieci Web na platformie Azure oraz lokalne repozytorium git używane do wdrażania plików w nowej witrynie sieci Web.</span><span class="sxs-lookup"><span data-stu-id="10048-111">This example creates a new website in Azure and a local Git repository to use for deploying files to the new website.</span></span>

### <span data-ttu-id="10048-112">Przykład 2: Tworzenie witryny sieci Web zintegrowanej z usługą GitHub</span><span class="sxs-lookup"><span data-stu-id="10048-112">Example 2: Create website integrated with GitHub</span></span>
```
PS C:\> New-AzureWebsite mysite -GitHub -GitHubRepository myaccount/myrepo
```

<span data-ttu-id="10048-113">W tym przykładzie jest tworzona nowa witryna sieci Web połączona z repozytorium GitHub o nazwie Moje konto/moje repozytorium.</span><span class="sxs-lookup"><span data-stu-id="10048-113">This example creates a new website linked to a GitHub repository named myaccount/myrepo.</span></span>
<span data-ttu-id="10048-114">Zatwierdzanie repozytorium GitHub jest przekazywane do witryny sieci Web na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="10048-114">Commits to the GitHub repository are pushed to the website in Azure.</span></span>

## <span data-ttu-id="10048-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="10048-115">PARAMETERS</span></span>

### <span data-ttu-id="10048-116">-Git</span><span class="sxs-lookup"><span data-stu-id="10048-116">-Git</span></span>
<span data-ttu-id="10048-117">Konfiguruje lokalne repozytorium git i łączy je z witryną internetową.</span><span class="sxs-lookup"><span data-stu-id="10048-117">Sets up a local Git repository and links it to the website.</span></span>
<span data-ttu-id="10048-118">W przypadku określenia tego parametru ten parametr konfiguruje repozytorium Git w katalogu lokalnym i dodanie repozytorium zdalnego o nazwie "Azure" połączonego z witryną internetową na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="10048-118">If specified, this parameter sets up a Git repository in the local directory and add a remote repository named 'azure' that links to the website in Azure.</span></span>

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

### <span data-ttu-id="10048-119">-GitHub</span><span class="sxs-lookup"><span data-stu-id="10048-119">-GitHub</span></span>
<span data-ttu-id="10048-120">Wskazuje, że to polecenie cmdlet łączy nową witrynę sieci Web z istniejącym repozytorium GitHub.</span><span class="sxs-lookup"><span data-stu-id="10048-120">Indicates that this cmdlet links the new website to an existing GitHub repository.</span></span>
<span data-ttu-id="10048-121">Zatwierdzanie repozytorium Giuthub jest przekazywane do witryny sieci Web na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="10048-121">Commits to the Giuthub repository are pushed to the website in Azure.</span></span>

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

### <span data-ttu-id="10048-122">-GitHubCredentials</span><span class="sxs-lookup"><span data-stu-id="10048-122">-GitHubCredentials</span></span>
<span data-ttu-id="10048-123">Określa poświadczenia nazwy użytkownika i hasła w celu nawiązania połączenia z usługą GitHub.</span><span class="sxs-lookup"><span data-stu-id="10048-123">Specifies the user name and password credentials to connect to GitHub.</span></span>

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

### <span data-ttu-id="10048-124">-GitHubRepository</span><span class="sxs-lookup"><span data-stu-id="10048-124">-GitHubRepository</span></span>
<span data-ttu-id="10048-125">Określa pełną nazwę repozytorium GitHub, które ma zostać połączone z tą witryną internetową.</span><span class="sxs-lookup"><span data-stu-id="10048-125">Specifies the full name of the GitHub repository to link to this website.</span></span>
<span data-ttu-id="10048-126">Na przykład `myaccount/myrepo` .</span><span class="sxs-lookup"><span data-stu-id="10048-126">For example, `myaccount/myrepo`.</span></span>

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

### <span data-ttu-id="10048-127">-Hostname</span><span class="sxs-lookup"><span data-stu-id="10048-127">-Hostname</span></span>
<span data-ttu-id="10048-128">Określa alternatywną nazwę hosta dla nowej witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="10048-128">Specifies an alternative host name for the new website.</span></span>

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

### <span data-ttu-id="10048-129">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="10048-129">-Location</span></span>
<span data-ttu-id="10048-130">Określa lokalizację centrum danych, w którym ma zostać wdrożona witryna sieci Web.</span><span class="sxs-lookup"><span data-stu-id="10048-130">Specifies the location of the data center where you want to deploy the website.</span></span>

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

### <span data-ttu-id="10048-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="10048-131">-Name</span></span>
<span data-ttu-id="10048-132">Określa nazwę witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="10048-132">Specifies a name for the website.</span></span>

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

### <span data-ttu-id="10048-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="10048-133">-Profile</span></span>
<span data-ttu-id="10048-134">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10048-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="10048-135">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="10048-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="10048-136">-PublishingUsername</span><span class="sxs-lookup"><span data-stu-id="10048-136">-PublishingUsername</span></span>
<span data-ttu-id="10048-137">Określa nazwę użytkownika określoną w portalu Azure dla wdrożenia git.</span><span class="sxs-lookup"><span data-stu-id="10048-137">Specifies the user name you have specified in the Azure Portal for Git deployment.</span></span>

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

### <span data-ttu-id="10048-138">-Slot</span><span class="sxs-lookup"><span data-stu-id="10048-138">-Slot</span></span>
<span data-ttu-id="10048-139">Określa nazwę gniazda witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="10048-139">Specifies a slot name for the website.</span></span>

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

### <span data-ttu-id="10048-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10048-140">CommonParameters</span></span>
<span data-ttu-id="10048-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10048-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10048-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10048-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10048-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10048-143">INPUTS</span></span>

## <span data-ttu-id="10048-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="10048-144">OUTPUTS</span></span>

## <span data-ttu-id="10048-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="10048-145">NOTES</span></span>

## <span data-ttu-id="10048-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10048-146">RELATED LINKS</span></span>

[<span data-ttu-id="10048-147">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="10048-147">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


