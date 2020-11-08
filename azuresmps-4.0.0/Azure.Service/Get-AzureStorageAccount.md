---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7D7D1FAE-5360-428B-AAE9-9D1109A7B67F
online version: ''
schema: 2.0.0
ms.openlocfilehash: faccd241929beca1f2423fa9c23f35793233205b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054515"
---
# <span data-ttu-id="c2b6c-101">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c2b6c-101">Get-AzureStorageAccount</span></span>

## <span data-ttu-id="c2b6c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b6c-103">Pobiera konta magazynu dla bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c2b6c-103">Gets the storage accounts for the current Azure subscription.</span></span>

## <span data-ttu-id="c2b6c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2b6c-104">SYNTAX</span></span>

```
Get-AzureStorageAccount [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c2b6c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c2b6c-105">DESCRIPTION</span></span>
<span data-ttu-id="c2b6c-106">Polecenie cmdlet **Get-AzureStorageAccount** zwraca obiekt zawierający informacje o kontach magazynu dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c2b6c-106">The **Get-AzureStorageAccount** cmdlet returns an object containing information about the storage accounts for the current subscription.</span></span>
<span data-ttu-id="c2b6c-107">Jeśli parametr *StorageAccountName* jest określony, zwracane są tylko informacje dotyczące określonego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="c2b6c-107">If the *StorageAccountName* parameter is specified, then only information about the specified storage account is returned.</span></span>

## <span data-ttu-id="c2b6c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2b6c-108">EXAMPLES</span></span>

### <span data-ttu-id="c2b6c-109">Przykład 1. zwraca wszystkie konta magazynu</span><span class="sxs-lookup"><span data-stu-id="c2b6c-109">Example 1: Return all storage accounts</span></span>
```
PS C:\> Get-AzureStorageAccount
```

<span data-ttu-id="c2b6c-110">To polecenie zwraca obiekt z wszystkimi kontami magazynu skojarzonymi z bieżącą subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="c2b6c-110">This command returns an object with all the storage accounts associated with the current subscription.</span></span>

### <span data-ttu-id="c2b6c-111">Przykład 2: informacje o koncie zwrotnym dla określonego konta</span><span class="sxs-lookup"><span data-stu-id="c2b6c-111">Example 2: Return account information for a specified account</span></span>
```
PS C:\> Get-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="c2b6c-112">To polecenie zwraca obiekt zawierający tylko informacje o koncie ContosoStore01.</span><span class="sxs-lookup"><span data-stu-id="c2b6c-112">This command returns an object with only the ContosoStore01 account information.</span></span>

### <span data-ttu-id="c2b6c-113">Przykład 3: wyświetlanie tabeli kont magazynu</span><span class="sxs-lookup"><span data-stu-id="c2b6c-113">Example 3: Display a table of storage accounts</span></span>
```
PS C:\> Get-AzureStorageAccount | Format-Table -AutoSize -Property @{Label="Name";Expression={$_.StorageAccountName}},"Label","Location"
```

<span data-ttu-id="c2b6c-114">To polecenie zwraca obiekt z wszystkimi kontami magazynu skojarzonymi z bieżącą subskrypcją i wyświetla go jako tabelę zawierającą nazwę konta, etykietę konta i lokalizację magazynu.</span><span class="sxs-lookup"><span data-stu-id="c2b6c-114">This command returns an object with all the storage accounts associated with the current subscription, and outputs them as a table showing the account name, the account label, and the storage location.</span></span>

## <span data-ttu-id="c2b6c-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2b6c-115">PARAMETERS</span></span>

### <span data-ttu-id="c2b6c-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c2b6c-116">-InformationAction</span></span>
<span data-ttu-id="c2b6c-117">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="c2b6c-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c2b6c-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c2b6c-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c2b6c-119">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="c2b6c-119">Continue</span></span>
- <span data-ttu-id="c2b6c-120">Ignorować</span><span class="sxs-lookup"><span data-stu-id="c2b6c-120">Ignore</span></span>
- <span data-ttu-id="c2b6c-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="c2b6c-121">Inquire</span></span>
- <span data-ttu-id="c2b6c-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c2b6c-122">SilentlyContinue</span></span>
- <span data-ttu-id="c2b6c-123">Przestaw</span><span class="sxs-lookup"><span data-stu-id="c2b6c-123">Stop</span></span>
- <span data-ttu-id="c2b6c-124">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="c2b6c-124">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b6c-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c2b6c-125">-InformationVariable</span></span>
<span data-ttu-id="c2b6c-126">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="c2b6c-126">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b6c-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="c2b6c-127">-Profile</span></span>
<span data-ttu-id="c2b6c-128">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2b6c-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c2b6c-129">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="c2b6c-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c2b6c-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c2b6c-130">-StorageAccountName</span></span>
<span data-ttu-id="c2b6c-131">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="c2b6c-131">Specifies the name of a storage account.</span></span>
<span data-ttu-id="c2b6c-132">Jeśli ta funkcja jest określona, to polecenie cmdlet zwróci tylko określony obiekt konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="c2b6c-132">If specified, this cmdlet returns only the specified storage account object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b6c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b6c-133">CommonParameters</span></span>
<span data-ttu-id="c2b6c-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2b6c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b6c-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2b6c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b6c-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2b6c-136">INPUTS</span></span>

## <span data-ttu-id="c2b6c-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2b6c-137">OUTPUTS</span></span>

### <span data-ttu-id="c2b6c-138">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="c2b6c-138">ManagementOperationContext</span></span>

## <span data-ttu-id="c2b6c-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2b6c-139">NOTES</span></span>
* <span data-ttu-id="c2b6c-140">Wpisz `help node-dev` , aby uzyskać pomoc dotyczącą Node.js poleceń cmdlet związanych z programowaniem.</span><span class="sxs-lookup"><span data-stu-id="c2b6c-140">Type `help node-dev` to get help on Node.js development-related cmdlets.</span></span> <span data-ttu-id="c2b6c-141">Wpisz `help php-dev` , aby uzyskać pomoc dotyczącą poleceń cmdlet związanych z projektowaniem w programie php.</span><span class="sxs-lookup"><span data-stu-id="c2b6c-141">Type `help php-dev` to get help on PHP development-related cmdlets.</span></span>

## <span data-ttu-id="c2b6c-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2b6c-142">RELATED LINKS</span></span>

[<span data-ttu-id="c2b6c-143">Nowe — AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c2b6c-143">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="c2b6c-144">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c2b6c-144">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


