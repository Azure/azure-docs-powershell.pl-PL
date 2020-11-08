---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A1E143A8-70F2-4158-9A10-F2082AD62A73
online version: ''
schema: 2.0.0
ms.openlocfilehash: 371291f4bd33809bc2f5880e4380c448219ed37a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054978"
---
# <span data-ttu-id="ebecf-101">Stop-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="ebecf-101">Stop-AzureStorSimpleJob</span></span>

## <span data-ttu-id="ebecf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ebecf-102">SYNOPSIS</span></span>
<span data-ttu-id="ebecf-103">Zatrzymuje zadanie programu StorSimple.</span><span class="sxs-lookup"><span data-stu-id="ebecf-103">Stops a StorSimple job.</span></span>

## <span data-ttu-id="ebecf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ebecf-104">SYNTAX</span></span>

```
Stop-AzureStorSimpleJob -InstanceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ebecf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ebecf-105">DESCRIPTION</span></span>
<span data-ttu-id="ebecf-106">Polecenie cmdlet **stop-AzureStorSimpleJob** zatrzymuje bieżące zadanie StorSimple.</span><span class="sxs-lookup"><span data-stu-id="ebecf-106">The **Stop-AzureStorSimpleJob** cmdlet stops an on-going StorSimple job.</span></span>
<span data-ttu-id="ebecf-107">Możesz określić zadania, podając identyfikator wystąpienia lub nazwę zadania.</span><span class="sxs-lookup"><span data-stu-id="ebecf-107">You can specify a jobs by supplying an instance ID or a job name.</span></span>

## <span data-ttu-id="ebecf-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ebecf-108">EXAMPLES</span></span>

### <span data-ttu-id="ebecf-109">Przykład 1: zatrzymywanie zadań dla urządzenia</span><span class="sxs-lookup"><span data-stu-id="ebecf-109">Example 1: Stop jobs for a device</span></span>
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" | Stop-AzureStorSimpleJob -Force
```

<span data-ttu-id="ebecf-110">To polecenie pobiera zadania dla urządzenia o nazwie Device07 przy użyciu polecenia cmdlet **Get-AzureStorSimpleJob** .</span><span class="sxs-lookup"><span data-stu-id="ebecf-110">This command gets the jobs for the device named Device07, by using the **Get-AzureStorSimpleJob** cmdlet.</span></span>
<span data-ttu-id="ebecf-111">Polecenie przekazuje zadania do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="ebecf-111">The command passes the jobs to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ebecf-112">Bieżące polecenie cmdlet zatrzymuje wszystkie zadania przekazywane do tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="ebecf-112">The current cmdlet stops any jobs that the command passes to it.</span></span>
<span data-ttu-id="ebecf-113">Polecenie określa parametr *Force* , a więc nie monituje o potwierdzenie przed zatrzymaniem zadania.</span><span class="sxs-lookup"><span data-stu-id="ebecf-113">The command specifies the *Force* parameter, and, so, it does not prompt you for confirmation before it stops a job.</span></span>

### <span data-ttu-id="ebecf-114">Przykład 2: zatrzymywanie określonego zadania</span><span class="sxs-lookup"><span data-stu-id="ebecf-114">Example 2: Stop a specific job</span></span>
```
PS C:\>Stop-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d" -Force
```

<span data-ttu-id="ebecf-115">To polecenie zatrzymuje zadanie o określonym IDENTYFIKATORze wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="ebecf-115">This command stops the job that has the specified instance ID.</span></span>

## <span data-ttu-id="ebecf-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ebecf-116">PARAMETERS</span></span>

### <span data-ttu-id="ebecf-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ebecf-117">-Force</span></span>
<span data-ttu-id="ebecf-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ebecf-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ebecf-119">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="ebecf-119">-InstanceId</span></span>
<span data-ttu-id="ebecf-120">Określa identyfikator zadania urządzenia, które ma zostać zatrzymane.</span><span class="sxs-lookup"><span data-stu-id="ebecf-120">Specifies the ID of the device job to stop.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebecf-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="ebecf-121">-Profile</span></span>
<span data-ttu-id="ebecf-122">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ebecf-122">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="ebecf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebecf-123">CommonParameters</span></span>
<span data-ttu-id="ebecf-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebecf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebecf-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebecf-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebecf-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ebecf-126">INPUTS</span></span>

### <span data-ttu-id="ebecf-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ebecf-127">None</span></span>

## <span data-ttu-id="ebecf-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ebecf-128">OUTPUTS</span></span>

### <span data-ttu-id="ebecf-129">DeviceJobDetails</span><span class="sxs-lookup"><span data-stu-id="ebecf-129">DeviceJobDetails</span></span>
<span data-ttu-id="ebecf-130">To polecenie cmdlet pobiera szczegóły **DeviceJob** , które zostanie zatrzymane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebecf-130">This cmdlet gets details of the **DeviceJob** that this cmdlet stops.</span></span>

## <span data-ttu-id="ebecf-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ebecf-131">NOTES</span></span>

## <span data-ttu-id="ebecf-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ebecf-132">RELATED LINKS</span></span>

[<span data-ttu-id="ebecf-133">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="ebecf-133">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


