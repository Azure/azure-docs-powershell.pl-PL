---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 679452A6-A6CA-4DC8-8E00-09E369505319
online version: ''
schema: 2.0.0
ms.openlocfilehash: 933c6de8e7baa55b2093a7ffc4ac28fede13bb5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055424"
---
# <span data-ttu-id="26a0f-101">Remove-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="26a0f-101">Remove-AzureStorageAccount</span></span>

## <span data-ttu-id="26a0f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="26a0f-102">SYNOPSIS</span></span>
<span data-ttu-id="26a0f-103">Usuwa określone konto magazynu z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="26a0f-103">Deletes the specified storage account from a subscription.</span></span>

## <span data-ttu-id="26a0f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="26a0f-104">SYNTAX</span></span>

```
Remove-AzureStorageAccount [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="26a0f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="26a0f-105">DESCRIPTION</span></span>
<span data-ttu-id="26a0f-106">Polecenie cmdlet **Remove-AzureStorageAccount** usuwa konto z subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="26a0f-106">The **Remove-AzureStorageAccount** cmdlet removes an account from an Azure subscription.</span></span>

## <span data-ttu-id="26a0f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="26a0f-107">EXAMPLES</span></span>

### <span data-ttu-id="26a0f-108">Przykład 1: usuwanie konta magazynu</span><span class="sxs-lookup"><span data-stu-id="26a0f-108">Example 1: Remove a storage account</span></span>
```
PS C:\> Remove-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="26a0f-109">To polecenie usuwa konto magazynu ContosoStore01 z określonego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="26a0f-109">This command removes the ContosoStore01 storage account from the specified subscription.</span></span>

## <span data-ttu-id="26a0f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26a0f-110">PARAMETERS</span></span>

### <span data-ttu-id="26a0f-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="26a0f-111">-InformationAction</span></span>
<span data-ttu-id="26a0f-112">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="26a0f-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="26a0f-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="26a0f-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="26a0f-114">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="26a0f-114">Continue</span></span>
- <span data-ttu-id="26a0f-115">Ignorować</span><span class="sxs-lookup"><span data-stu-id="26a0f-115">Ignore</span></span>
- <span data-ttu-id="26a0f-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="26a0f-116">Inquire</span></span>
- <span data-ttu-id="26a0f-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="26a0f-117">SilentlyContinue</span></span>
- <span data-ttu-id="26a0f-118">Przestaw</span><span class="sxs-lookup"><span data-stu-id="26a0f-118">Stop</span></span>
- <span data-ttu-id="26a0f-119">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="26a0f-119">Suspend</span></span>

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

### <span data-ttu-id="26a0f-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="26a0f-120">-InformationVariable</span></span>
<span data-ttu-id="26a0f-121">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="26a0f-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="26a0f-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="26a0f-122">-Profile</span></span>
<span data-ttu-id="26a0f-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26a0f-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="26a0f-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="26a0f-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="26a0f-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="26a0f-125">-StorageAccountName</span></span>
<span data-ttu-id="26a0f-126">Określa nazwę konta magazynu, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="26a0f-126">Specifies the name of the storage account to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26a0f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26a0f-127">CommonParameters</span></span>
<span data-ttu-id="26a0f-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26a0f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26a0f-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26a0f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26a0f-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26a0f-130">INPUTS</span></span>

## <span data-ttu-id="26a0f-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="26a0f-131">OUTPUTS</span></span>

## <span data-ttu-id="26a0f-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="26a0f-132">NOTES</span></span>

## <span data-ttu-id="26a0f-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26a0f-133">RELATED LINKS</span></span>

[<span data-ttu-id="26a0f-134">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="26a0f-134">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="26a0f-135">Nowe — AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="26a0f-135">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="26a0f-136">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="26a0f-136">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


