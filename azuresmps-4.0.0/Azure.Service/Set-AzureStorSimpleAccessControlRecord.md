---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 71CFCA9D-198E-481A-BB85-159477F25322
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2c050ea91cc85a89702fb6cf62f05779db7155e4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054824"
---
# <span data-ttu-id="46dec-101">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="46dec-101">Set-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="46dec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="46dec-102">SYNOPSIS</span></span>
<span data-ttu-id="46dec-103">Aktualizuje nazwę IQN rekordu kontroli dostępu.</span><span class="sxs-lookup"><span data-stu-id="46dec-103">Updates the IQN of an access control record.</span></span>

## <span data-ttu-id="46dec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="46dec-104">SYNTAX</span></span>

```
Set-AzureStorSimpleAccessControlRecord -ACRName <String> -IQNInitiatorName <String> [-WaitForComplete]
 [-NewName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="46dec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="46dec-105">DESCRIPTION</span></span>
<span data-ttu-id="46dec-106">Polecenie cmdlet **Set-AzureStorSimpleAccessControlRecord** aktualizuje kwalifikowaną nazwę iSCSI (IQN) istniejącego rekordu kontroli dostępu.</span><span class="sxs-lookup"><span data-stu-id="46dec-106">The **Set-AzureStorSimpleAccessControlRecord** cmdlet updates the iSCSI qualified name (IQN) of an existing access control record.</span></span>

## <span data-ttu-id="46dec-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="46dec-107">EXAMPLES</span></span>

### <span data-ttu-id="46dec-108">Przykład 1: aktualizowanie rekordu kontroli dostępu</span><span class="sxs-lookup"><span data-stu-id="46dec-108">Example 1: Update an access control record</span></span>
```
PS C:\>Set-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -IQNInitiatorName "IqnUpdated" -WaitForComplete
VERBOSE: ClientRequestId: e4766335-f302-40e0-93bf-fad7aa488ae6_PS
VERBOSE: ClientRequestId: cfdbbd67-6ba5-4238-b743-b88f604079b9_PS
VERBOSE: About to run a task to update your Access Control Record! 
VERBOSE: ClientRequestId: d5cf2793-0ab5-40ff-ab6f-43e21bc4c0a4_PS


JobId        : 89502523-52fc-4ce2-b2d4-cb8c6692fb60
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your update operation has completed successfully. 
VERBOSE: ClientRequestId: cbd47519-3a3c-4365-b097-0fb7551c48ee_PS
GlobalId            : 
InitiatorName       : IqnUpdated
InstanceId          : 9bcfbc83-e196-4688-9016-827f51515c24
Name                : Acr10
OperationInProgress : None
VolumeCount         : 0
```

<span data-ttu-id="46dec-109">To polecenie aktualizuje rekord kontroli dostępu o nazwie Acr10 dla inicjatora iSCSI o nazwie IqnUpdated.</span><span class="sxs-lookup"><span data-stu-id="46dec-109">This command updates the access control record named Acr10 for the iSCSI initiator named IqnUpdated.</span></span>
<span data-ttu-id="46dec-110">To polecenie określa parametr *WaitForComplete* , a więc polecenie czeka na zakończenie operacji, a następnie zwraca obiekt **TaskStatusInfo** .</span><span class="sxs-lookup"><span data-stu-id="46dec-110">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

## <span data-ttu-id="46dec-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46dec-111">PARAMETERS</span></span>

### <span data-ttu-id="46dec-112">-ACRName</span><span class="sxs-lookup"><span data-stu-id="46dec-112">-ACRName</span></span>
<span data-ttu-id="46dec-113">Określa nazwę rekordu kontroli dostępu do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="46dec-113">Specifies a name of the access control record to modify.</span></span>

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

### <span data-ttu-id="46dec-114">-IQNInitiatorName</span><span class="sxs-lookup"><span data-stu-id="46dec-114">-IQNInitiatorName</span></span>
<span data-ttu-id="46dec-115">Określa nazwę IQN inicjatora iSCSI, dla którego ten aplet polecenia zapewnia dostęp do woluminu.</span><span class="sxs-lookup"><span data-stu-id="46dec-115">Specifies the IQN of the iSCSI initiator to which this cmdlet provides access for the volume.</span></span>

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

### <span data-ttu-id="46dec-116">-NewName</span><span class="sxs-lookup"><span data-stu-id="46dec-116">-NewName</span></span>
<span data-ttu-id="46dec-117">Określa nową nazwę rekordu kontroli dostępu.</span><span class="sxs-lookup"><span data-stu-id="46dec-117">Specifies a new name for access control record.</span></span>

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

### <span data-ttu-id="46dec-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="46dec-118">-Profile</span></span>
<span data-ttu-id="46dec-119">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="46dec-119">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="46dec-120">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="46dec-120">-WaitForComplete</span></span>
<span data-ttu-id="46dec-121">Wskazuje, że przed zwróceniem kontroli na konsolę programu Windows PowerShell to polecenie cmdlet oczekuje na ukończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="46dec-121">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="46dec-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46dec-122">CommonParameters</span></span>
<span data-ttu-id="46dec-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46dec-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46dec-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46dec-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46dec-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46dec-125">INPUTS</span></span>

### <span data-ttu-id="46dec-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="46dec-126">None</span></span>

## <span data-ttu-id="46dec-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="46dec-127">OUTPUTS</span></span>

### <span data-ttu-id="46dec-128">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="46dec-128">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="46dec-129">To polecenie cmdlet zwraca obiekt **TaskStatusInfo** , jeśli określisz parametr *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="46dec-129">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="46dec-130">Jeśli nie określisz tego parametru, zwraca obiekt **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="46dec-130">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="46dec-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="46dec-131">NOTES</span></span>

## <span data-ttu-id="46dec-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46dec-132">RELATED LINKS</span></span>

[<span data-ttu-id="46dec-133">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="46dec-133">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="46dec-134">Nowe — AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="46dec-134">New-AzureStorSimpleAccessControlRecord</span></span>](./New-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="46dec-135">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="46dec-135">Remove-AzureStorSimpleAccessControlRecord</span></span>](./Remove-AzureStorSimpleAccessControlRecord.md)


