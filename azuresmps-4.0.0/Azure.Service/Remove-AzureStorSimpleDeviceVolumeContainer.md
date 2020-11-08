---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: C50959BB-7481-4898-BF4B-C5ABF8758473
online version: ''
schema: 2.0.0
ms.openlocfilehash: e2c06455004afbd15235f59164034abc2147964b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055419"
---
# <span data-ttu-id="d3f4b-101">Remove-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="d3f4b-101">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="d3f4b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d3f4b-102">SYNOPSIS</span></span>
<span data-ttu-id="d3f4b-103">Usuwa kontener woluminu z urządzenia StorSimple.</span><span class="sxs-lookup"><span data-stu-id="d3f4b-103">Removes a volume container from a StorSimple device.</span></span>

## <span data-ttu-id="d3f4b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d3f4b-104">SYNTAX</span></span>

```
Remove-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> -VolumeContainer <DataContainer>
 [-WaitForComplete] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d3f4b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d3f4b-105">DESCRIPTION</span></span>
<span data-ttu-id="d3f4b-106">Polecenie cmdlet **Remove-AzureStorSimpleDeviceVolumeContainer** usuwa obiekt kontenera woluminu z urządzenia StorSimple.</span><span class="sxs-lookup"><span data-stu-id="d3f4b-106">The **Remove-AzureStorSimpleDeviceVolumeContainer** cmdlet removes a volume container object from a StorSimple device.</span></span>
<span data-ttu-id="d3f4b-107">To polecenie cmdlet monituje o potwierdzenie, o ile nie określi się parametru *Force* .</span><span class="sxs-lookup"><span data-stu-id="d3f4b-107">This cmdlet prompts you for confirmation unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="d3f4b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d3f4b-108">EXAMPLES</span></span>

### <span data-ttu-id="d3f4b-109">Przykład 1: usuwanie kontenera przy użyciu rurociągu</span><span class="sxs-lookup"><span data-stu-id="d3f4b-109">Example 1: Remove a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08" | Remove-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -Force
VERBOSE: ClientRequestId: 0efbb4fc-ceb0-4311-bc49-0e08161d0a37_PS
VERBOSE: ClientRequestId: bf5b615f-47e3-4868-91b6-f2d12217a302_PS
VERBOSE: ClientRequestId: 5590c87e-0602-4197-b6c3-cf58b0e7a7b3_PS
VERBOSE: ClientRequestId: b33c71ac-c345-44ff-8213-d7fdf9f8480a_PS
VERBOSE: ClientRequestId: 903d42ef-58f4-4e89-ba7f-5f234262356d_PS
VERBOSE: About to create a job to remove your Volume container! 
VERBOSE: ClientRequestId: 2279575f-5115-4344-9c6f-9ef599bd203e_PS
e9ddec89-67ac-4e2e-a2ed-820de3547bb0
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
e9ddec89-67ac-4e2e-a2ed-820de3547bb0 for tracking the task's status
VERBOSE: Volume container with name: Container08 is found.
```

<span data-ttu-id="d3f4b-110">To polecenie pobiera kontener woluminu o nazwie Container08 na urządzeniu o nazwie Contoso63-AppVm przy użyciu polecenia cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="d3f4b-110">This command gets the volume container named Container08 on the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="d3f4b-111">Polecenie przekazuje kontener woluminu do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="d3f4b-111">The command passes the volume container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d3f4b-112">To polecenie rozpoczyna zadanie usunięcia kontenera, a następnie zwraca obiekt **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="d3f4b-112">This command starts the task to remove the container, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="d3f4b-113">Aby sprawdzić stan zadania, użyj polecenia cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="d3f4b-113">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>
<span data-ttu-id="d3f4b-114">To polecenie określa parametr *Force* , więc nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d3f4b-114">This command specifies the *Force* parameter, so it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="d3f4b-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d3f4b-115">PARAMETERS</span></span>

### <span data-ttu-id="d3f4b-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d3f4b-116">-DeviceName</span></span>
<span data-ttu-id="d3f4b-117">Określa nazwę urządzenia StorSimple, na którym ma zostać usunięty kontener woluminu, istnieje.</span><span class="sxs-lookup"><span data-stu-id="d3f4b-117">Specifies the name of the StorSimple device on which to the volume container to remove exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3f4b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d3f4b-118">-Force</span></span>
<span data-ttu-id="d3f4b-119">Wskazuje, że w tym poleceniu cmdlet nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d3f4b-119">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="d3f4b-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="d3f4b-120">-Profile</span></span>
<span data-ttu-id="d3f4b-121">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d3f4b-121">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="d3f4b-122">-VolumeContainer</span><span class="sxs-lookup"><span data-stu-id="d3f4b-122">-VolumeContainer</span></span>
<span data-ttu-id="d3f4b-123">Określa kontener woluminu, który ma zostać usunięty, jako obiekt kontenera **datacontainer** .</span><span class="sxs-lookup"><span data-stu-id="d3f4b-123">Specifies the volume container to remove, as a **DataContainer** object.</span></span>
<span data-ttu-id="d3f4b-124">Aby uzyskać obiekt **kontenera datakontener** , użyj polecenia cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="d3f4b-124">To obtain a **DataContainer** object, use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f4b-125">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="d3f4b-125">-WaitForComplete</span></span>
<span data-ttu-id="d3f4b-126">Wskazuje, że przed zwróceniem kontroli na konsolę programu Windows PowerShell to polecenie cmdlet oczekuje na ukończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="d3f4b-126">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="d3f4b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f4b-127">CommonParameters</span></span>
<span data-ttu-id="d3f4b-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3f4b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f4b-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3f4b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f4b-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3f4b-130">INPUTS</span></span>

### <span data-ttu-id="d3f4b-131">Kontenery</span><span class="sxs-lookup"><span data-stu-id="d3f4b-131">DataContainer</span></span>
<span data-ttu-id="d3f4b-132">To polecenie cmdlet umożliwia akceptowanie usunięcia obiektu **datakontenera** .</span><span class="sxs-lookup"><span data-stu-id="d3f4b-132">This cmdlet accepts a **DataContainer** object to remove.</span></span>

## <span data-ttu-id="d3f4b-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d3f4b-133">OUTPUTS</span></span>

### <span data-ttu-id="d3f4b-134">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="d3f4b-134">TaskStatusInfo</span></span>
<span data-ttu-id="d3f4b-135">To polecenie cmdlet zwraca obiekt **TaskStatusInfo** , jeśli określisz parametr *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="d3f4b-135">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="d3f4b-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d3f4b-136">NOTES</span></span>

## <span data-ttu-id="d3f4b-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3f4b-137">RELATED LINKS</span></span>

[<span data-ttu-id="d3f4b-138">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="d3f4b-138">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="d3f4b-139">Nowe — AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="d3f4b-139">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)


