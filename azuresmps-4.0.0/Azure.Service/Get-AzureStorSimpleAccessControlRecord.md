---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 71302FB6-7E2B-4972-A743-AB537AC7CD79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79e194e0f8dda4392dec191881702c680bf172ac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055518"
---
# <span data-ttu-id="be975-101">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="be975-101">Get-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="be975-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="be975-102">SYNOPSIS</span></span>
<span data-ttu-id="be975-103">Pobiera rekordy kontroli dostępu w konfiguracji usługi.</span><span class="sxs-lookup"><span data-stu-id="be975-103">Gets access control records in a service configuration.</span></span>

## <span data-ttu-id="be975-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="be975-104">SYNTAX</span></span>

```
Get-AzureStorSimpleAccessControlRecord [-ACRName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="be975-105">Opis</span><span class="sxs-lookup"><span data-stu-id="be975-105">DESCRIPTION</span></span>
<span data-ttu-id="be975-106">Polecenie cmdlet **Get-AzureStorSimpleAccessControlRecord** pobiera rekordy kontroli dostępu w konfiguracji usługi StorSimple Manager.</span><span class="sxs-lookup"><span data-stu-id="be975-106">The **Get-AzureStorSimpleAccessControlRecord** cmdlet gets access control records in the StorSimple Manager service configuration.</span></span>
<span data-ttu-id="be975-107">To polecenie cmdlet pobiera wszystkie rekordy lub nazwany rekord.</span><span class="sxs-lookup"><span data-stu-id="be975-107">This cmdlet gets all records or a named record.</span></span>

<span data-ttu-id="be975-108">Rekordy kontroli dostępu są kontenerami parametrów inicjatora iSCSI.</span><span class="sxs-lookup"><span data-stu-id="be975-108">Access control records are containers of iSCSI initiator parameters.</span></span>
<span data-ttu-id="be975-109">Te parametry określają, którzy inicjatorzy mogą uzyskać dostęp do woluminu.</span><span class="sxs-lookup"><span data-stu-id="be975-109">These parameters specify which initiators can access a volume.</span></span>
<span data-ttu-id="be975-110">Gdy inicjator iSCSI próbuje połączyć się z woluminem, urządzenie sprawdza rekordy kontroli dostępu przypisane do tego woluminu.</span><span class="sxs-lookup"><span data-stu-id="be975-110">When an iSCSI initiator attempts to connect to a volume, your appliance checks the access control records assigned to that volume.</span></span>
<span data-ttu-id="be975-111">Jeśli parametry inicjatora iSCSI pasują do jednego z wpisów w rekordzie kontroli dostępu zamapowanym na ten wolumin, inicjator iSCSI może nawiązywać połączenie.</span><span class="sxs-lookup"><span data-stu-id="be975-111">If the iSCSI initiator parameters match one of the entries in an access control record mapped to that volume, the iSCSI initiator can connect.</span></span>

## <span data-ttu-id="be975-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="be975-112">EXAMPLES</span></span>

### <span data-ttu-id="be975-113">Przykład 1. pobieranie wszystkich rekordów kontroli dostępu</span><span class="sxs-lookup"><span data-stu-id="be975-113">Example 1: Get all access control records</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord
InstanceId                           Name                        InitiatorName               VolumeCount
----------                           ----                        -------------               -----------
01a31aa5-14de-4b77-b926-2842577f540e Windows_XYUSFL718-RV_ACR    iqn.1991-05.com.microsof... 3
071c282d-0cd2-4c5f-b687-48966037ba48 Linux_XYUSFL719_ACR         iqn.1994-05.com.redhat:a... 3
4600eade-71f8-4d04-baec-0e7cf1d1e8fb Windows_XYUSFL720_ACR       iqn.1991-05.com.microsof... 9
d508d6f0-fcda-4624-b223-c0b307d6113e Linux_XYUSFL350_ACR         iqn.1991-05.com.microsof... 9
```

<span data-ttu-id="be975-114">To polecenie pobiera wszystkie rekordy kontroli dostępu.</span><span class="sxs-lookup"><span data-stu-id="be975-114">This command gets all access control records.</span></span>

### <span data-ttu-id="be975-115">Przykład 2: uzyskiwanie określonego rekordu kontroli dostępu</span><span class="sxs-lookup"><span data-stu-id="be975-115">Example 2: Get a specific access control record</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr11"
VERBOSE: ClientRequestId: 61f261c7-acd3-4bcc-922a-ddfd85eb767b_PS
VERBOSE: ClientRequestId: 49c6a4c7-d299-46fd-a553-034c52b47487_PS

GlobalId            : 
InitiatorName       : iqn-contoso63
InstanceId          : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
Name                : Acr11
OperationInProgress : None
VolumeCount         : 6

VERBOSE: Access Control Record with given name Acr11 is found!
```

<span data-ttu-id="be975-116">To polecenie uzyskuje rekord kontroli dostępu o nazwie Acr11.</span><span class="sxs-lookup"><span data-stu-id="be975-116">This command gets the access control record named Acr11.</span></span>

## <span data-ttu-id="be975-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="be975-117">PARAMETERS</span></span>

### <span data-ttu-id="be975-118">-ACRName</span><span class="sxs-lookup"><span data-stu-id="be975-118">-ACRName</span></span>
<span data-ttu-id="be975-119">Określa nazwę rekordu kontroli dostępu, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="be975-119">Specifies the name of an access control record to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be975-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="be975-120">-Profile</span></span>
<span data-ttu-id="be975-121">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="be975-121">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="be975-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be975-122">CommonParameters</span></span>
<span data-ttu-id="be975-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be975-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be975-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be975-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be975-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be975-125">INPUTS</span></span>

### <span data-ttu-id="be975-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="be975-126">None</span></span>

## <span data-ttu-id="be975-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="be975-127">OUTPUTS</span></span>

### <span data-ttu-id="be975-128">AccessControlRecord, IList\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="be975-128">AccessControlRecord, IList\<AccessControlRecord\></span></span>
<span data-ttu-id="be975-129">To polecenie cmdlet zwraca obiekt **AccessControlRecord** lub obiekt **IList \<AccessControlRecord\>** .</span><span class="sxs-lookup"><span data-stu-id="be975-129">This cmdlet returns an **AccessControlRecord** object or an **IList\<AccessControlRecord\>** object.</span></span>
<span data-ttu-id="be975-130">Obiekt **AccessControlRecord** zawiera następujące pola:</span><span class="sxs-lookup"><span data-stu-id="be975-130">An **AccessControlRecord** object contains the following fields:</span></span> 

- <span data-ttu-id="be975-131">**GlobalId** ( **ciąg** )</span><span class="sxs-lookup"><span data-stu-id="be975-131">**GlobalId** ( **String** )</span></span> 
- <span data-ttu-id="be975-132">**Initiatorname** ( **ciąg** )</span><span class="sxs-lookup"><span data-stu-id="be975-132">**InitiatorName** ( **String** )</span></span> 
- <span data-ttu-id="be975-133">**InstanceId** ( **ciąg** )</span><span class="sxs-lookup"><span data-stu-id="be975-133">**InstanceId** ( **String** )</span></span> 
- <span data-ttu-id="be975-134">**Name** ( **ciąg** )</span><span class="sxs-lookup"><span data-stu-id="be975-134">**Name** ( **String** )</span></span> 
- <span data-ttu-id="be975-135">**OperationInProgress** ( **OperationInProgress** )</span><span class="sxs-lookup"><span data-stu-id="be975-135">**OperationInProgress** ( **OperationInProgress** )</span></span> 
- <span data-ttu-id="be975-136">**VolumeCount** ( **int** )</span><span class="sxs-lookup"><span data-stu-id="be975-136">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="be975-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="be975-137">NOTES</span></span>

## <span data-ttu-id="be975-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be975-138">RELATED LINKS</span></span>

[<span data-ttu-id="be975-139">Nowe — AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="be975-139">New-AzureStorSimpleAccessControlRecord</span></span>](./New-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="be975-140">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="be975-140">Remove-AzureStorSimpleAccessControlRecord</span></span>](./Remove-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="be975-141">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="be975-141">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)


