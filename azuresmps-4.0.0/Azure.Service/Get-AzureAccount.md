---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 70ADAF16-BC52-47BF-A85A-A84DEACDA027
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2704dbdc308b9773452b05ceba24719f2e274132
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054642"
---
# <span data-ttu-id="56b45-101">Get-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="56b45-101">Get-AzureAccount</span></span>

## <span data-ttu-id="56b45-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56b45-102">SYNOPSIS</span></span>
<span data-ttu-id="56b45-103">Uzyskuje dostęp do kont platformy Azure dostępnych w usłudze Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="56b45-103">Gets Azure accounts that are available to Azure PowerShell.</span></span>

## <span data-ttu-id="56b45-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56b45-104">SYNTAX</span></span>

```
Get-AzureAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="56b45-105">Opis</span><span class="sxs-lookup"><span data-stu-id="56b45-105">DESCRIPTION</span></span>
<span data-ttu-id="56b45-106">Polecenie cmdlet **Get-AzureAccount** pobiera konta platformy Azure dostępne dla programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="56b45-106">The **Get-AzureAccount** cmdlet gets the Azure accounts that are available to Windows PowerShell.</span></span>
<span data-ttu-id="56b45-107">Aby udostępnić konta w programie Windows PowerShell, Użyj poleceń cmdlet **Add-AzureAccount** lub **Import-PublishSettingsFile** .</span><span class="sxs-lookup"><span data-stu-id="56b45-107">To make your accounts available to Windows PowerShell, use the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlets.</span></span>

## <span data-ttu-id="56b45-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56b45-108">EXAMPLES</span></span>

### <span data-ttu-id="56b45-109">Przykład 1: pobieranie wszystkich kont</span><span class="sxs-lookup"><span data-stu-id="56b45-109">Example 1: Get all accounts</span></span>
```
PS C:\> Get-AzureAccount

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
contosotest1@outlook.com     {{ ActiveDirectoryTenantId = aaeabcde-386c-4466-bf70-794...
```

<span data-ttu-id="56b45-110">To polecenie umożliwia pobieranie wszystkich kont skojarzonych z określonym użytkownikiem.</span><span class="sxs-lookup"><span data-stu-id="56b45-110">This command gets all accounts associated with the specified user.</span></span>

### <span data-ttu-id="56b45-111">Przykład 2: Uzyskiwanie konta według nazwy</span><span class="sxs-lookup"><span data-stu-id="56b45-111">Example 2: Get an account by name</span></span>
```
PS C:\> Get-AzureAccount -Name contosoadmin@outlook.com

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
```

<span data-ttu-id="56b45-112">To polecenie pobiera konto ContosoAdmin.</span><span class="sxs-lookup"><span data-stu-id="56b45-112">This command gets the ContosoAdmin account.</span></span>

## <span data-ttu-id="56b45-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56b45-113">PARAMETERS</span></span>

### <span data-ttu-id="56b45-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="56b45-114">-Name</span></span>
<span data-ttu-id="56b45-115">Pobiera tylko określone konto.</span><span class="sxs-lookup"><span data-stu-id="56b45-115">Gets only the specified account.</span></span>
<span data-ttu-id="56b45-116">Domyślnie wszystkie konta są dostępne w programie Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="56b45-116">The default is all accounts that are available to Windows PowerShell.</span></span>
<span data-ttu-id="56b45-117">Wprowadź nazwę konta.</span><span class="sxs-lookup"><span data-stu-id="56b45-117">Enter the account name.</span></span>
<span data-ttu-id="56b45-118">W wartości **nazwy** jest uwzględniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="56b45-118">The **Name** value is case-sensitive.</span></span>
<span data-ttu-id="56b45-119">Używanie symboli wieloznacznych jest niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="56b45-119">Wildcards are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56b45-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="56b45-120">-Profile</span></span>
<span data-ttu-id="56b45-121">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56b45-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="56b45-122">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="56b45-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="56b45-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56b45-123">CommonParameters</span></span>
<span data-ttu-id="56b45-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56b45-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56b45-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56b45-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56b45-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56b45-126">INPUTS</span></span>

### <span data-ttu-id="56b45-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="56b45-127">None</span></span>
<span data-ttu-id="56b45-128">Nie możesz popotokować danych wejściowych tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56b45-128">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="56b45-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56b45-129">OUTPUTS</span></span>

### <span data-ttu-id="56b45-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="56b45-130">None</span></span>
<span data-ttu-id="56b45-131">To polecenie cmdlet nie zwraca żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="56b45-131">This cmdlet does not return any output.</span></span>

## <span data-ttu-id="56b45-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56b45-132">NOTES</span></span>

## <span data-ttu-id="56b45-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56b45-133">RELATED LINKS</span></span>

[<span data-ttu-id="56b45-134">Dodaj-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="56b45-134">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="56b45-135">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="56b45-135">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="56b45-136">Import — AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="56b45-136">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="56b45-137">Remove-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="56b45-137">Remove-AzureAccount</span></span>](./Remove-AzureAccount.md)


