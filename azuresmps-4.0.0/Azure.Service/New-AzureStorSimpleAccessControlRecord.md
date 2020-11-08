---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: ED6CDEA3-0A5D-47E6-B9D7-47D1862212DF
online version: ''
schema: 2.0.0
ms.openlocfilehash: b907627200ec2463d997ebb4faa834e2821b1c7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055176"
---
# <span data-ttu-id="205c0-101">New-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="205c0-101">New-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="205c0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="205c0-102">SYNOPSIS</span></span>
<span data-ttu-id="205c0-103">Tworzy rekord kontroli dostępu.</span><span class="sxs-lookup"><span data-stu-id="205c0-103">Creates an access control record.</span></span>

## <span data-ttu-id="205c0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="205c0-104">SYNTAX</span></span>

```
New-AzureStorSimpleAccessControlRecord -ACRName <String> -IQNInitiatorName <String> [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="205c0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="205c0-105">DESCRIPTION</span></span>
<span data-ttu-id="205c0-106">Polecenie cmdlet **New-AzureStorSimpleAccessControlRecord** tworzy rekord kontroli dostępu.</span><span class="sxs-lookup"><span data-stu-id="205c0-106">The **New-AzureStorSimpleAccessControlRecord** cmdlet creates an access control record.</span></span>
<span data-ttu-id="205c0-107">Do konfigurowania woluminów można użyć obiektu **AccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="205c0-107">You can use an **AccessControlRecord** object to configure volumes.</span></span>

## <span data-ttu-id="205c0-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="205c0-108">EXAMPLES</span></span>

### <span data-ttu-id="205c0-109">Przykład 1. Tworzenie rekordu kontrolki programu Access Controlaccess i oczekiwanie na kontrolkę resultaccess</span><span class="sxs-lookup"><span data-stu-id="205c0-109">Example 1: Create an Access Controlaccess control record and wait for the resultaccess control</span></span>
```
PS C:\>New-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -IQNInitiatorName "Iqn10" -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 08719243-3a76-43a5-a88b-e5f2b63ed3d9
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e12362c2c06615108ba8436cf85fcd40
```

<span data-ttu-id="205c0-110">To polecenie tworzy rekord kontroli dostępu o nazwie Acr10 dla inicjatora iSCSI o nazwie Iqn10.</span><span class="sxs-lookup"><span data-stu-id="205c0-110">This command creates an access control record named Acr10 for the iSCSI initiator named Iqn10.</span></span>
<span data-ttu-id="205c0-111">To polecenie określa parametr *WaitForComplete* , a więc polecenie czeka na zakończenie operacji, a następnie zwraca obiekt **TaskStatusInfo** .</span><span class="sxs-lookup"><span data-stu-id="205c0-111">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="205c0-112">Przykład 2: Tworzenie formantu recordaccess kontrolki programu Access Controlaccess</span><span class="sxs-lookup"><span data-stu-id="205c0-112">Example 2: Create an Access Controlaccess control recordaccess control</span></span>
```
PS C:\>New-AzureStorSimpleAccessControlRecord -ACRName "Acr11" -IQNInitiatorName "Iqn11"
VERBOSE: The create job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
2bd56fbb-4b95-4f2c-b99f-6321231a018d for tracking the job status
```

<span data-ttu-id="205c0-113">To polecenie tworzy rekord kontroli dostępu o nazwie Acr11 dla inicjatora iSCSI o nazwie Iqn11.</span><span class="sxs-lookup"><span data-stu-id="205c0-113">This command creates an access control record named Acr11 for the iSCSI initiator named Iqn11.</span></span>
<span data-ttu-id="205c0-114">To polecenie nie określa parametru *WaitForComplete* , a więc polecenie rozpoczyna zadanie, a następnie zwraca obiekt **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="205c0-114">This command does not specify the *WaitForComplete* parameter, and, therefore, the command starts the task, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="205c0-115">Aby sprawdzić stan zadania, użyj polecenia cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="205c0-115">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="205c0-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="205c0-116">PARAMETERS</span></span>

### <span data-ttu-id="205c0-117">-ACRName</span><span class="sxs-lookup"><span data-stu-id="205c0-117">-ACRName</span></span>
<span data-ttu-id="205c0-118">Określa nazwę rekordu kontroli dostępu.</span><span class="sxs-lookup"><span data-stu-id="205c0-118">Specifies a name for the access control record.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205c0-119">-IQNInitiatorName</span><span class="sxs-lookup"><span data-stu-id="205c0-119">-IQNInitiatorName</span></span>
<span data-ttu-id="205c0-120">Określa kwalifikowaną nazwę iSCSI (IQN) inicjatora iSCSI, dla którego to polecenie cmdlet zapewnia dostęp do woluminu.</span><span class="sxs-lookup"><span data-stu-id="205c0-120">Specifies the iSCSI qualified name (IQN) of the iSCSI initiator to which this cmdlet provides access for the volume.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IQN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205c0-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="205c0-121">-Profile</span></span>
<span data-ttu-id="205c0-122">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="205c0-122">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="205c0-123">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="205c0-123">-WaitForComplete</span></span>
<span data-ttu-id="205c0-124">Wskazuje, że przed zwróceniem kontroli na konsolę programu Windows PowerShell to polecenie cmdlet oczekuje na ukończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="205c0-124">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205c0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="205c0-125">CommonParameters</span></span>
<span data-ttu-id="205c0-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="205c0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="205c0-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="205c0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="205c0-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="205c0-128">INPUTS</span></span>

### <span data-ttu-id="205c0-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="205c0-129">None</span></span>

## <span data-ttu-id="205c0-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="205c0-130">OUTPUTS</span></span>

### <span data-ttu-id="205c0-131">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="205c0-131">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="205c0-132">To polecenie cmdlet zwraca obiekt **TaskStatusInfo** , jeśli określisz parametr *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="205c0-132">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="205c0-133">Jeśli nie określisz tego parametru, zwraca obiekt **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="205c0-133">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="205c0-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="205c0-134">NOTES</span></span>

## <span data-ttu-id="205c0-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="205c0-135">RELATED LINKS</span></span>

[<span data-ttu-id="205c0-136">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="205c0-136">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="205c0-137">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="205c0-137">Remove-AzureStorSimpleAccessControlRecord</span></span>](./Remove-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="205c0-138">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="205c0-138">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="205c0-139">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="205c0-139">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


