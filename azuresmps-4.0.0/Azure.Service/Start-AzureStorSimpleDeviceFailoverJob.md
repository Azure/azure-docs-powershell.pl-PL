---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 53580FF1-D905-40FD-A5F0-D5FBCD036E0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a51fd8210d2fe7fb224ed43650a354e383ed4e54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054742"
---
# <span data-ttu-id="8fe39-101">Start-AzureStorSimpleDeviceFailoverJob</span><span class="sxs-lookup"><span data-stu-id="8fe39-101">Start-AzureStorSimpleDeviceFailoverJob</span></span>

## <span data-ttu-id="8fe39-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8fe39-102">SYNOPSIS</span></span>
<span data-ttu-id="8fe39-103">Inicjuje operację przejęcia awaryjnego grup kontenerów woluminów.</span><span class="sxs-lookup"><span data-stu-id="8fe39-103">Initiates a failover operation of volume container groups.</span></span>

## <span data-ttu-id="8fe39-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8fe39-104">SYNTAX</span></span>

### <span data-ttu-id="8fe39-105">Empty (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="8fe39-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8fe39-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="8fe39-106">IdentifyById</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceId <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8fe39-107">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="8fe39-107">IdentifyByName</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceName <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceName <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8fe39-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8fe39-108">DESCRIPTION</span></span>
<span data-ttu-id="8fe39-109">Polecenie cmdlet **Start-AzureStorSimpleDeviceFailoverJob** inicjuje działanie trybu failover jednej lub większej liczby grup kontenerów woluminów z jednego urządzenia na inny.</span><span class="sxs-lookup"><span data-stu-id="8fe39-109">The **Start-AzureStorSimpleDeviceFailoverJob** cmdlet initiates a failover operation of one or more volume container groups from one device to another.</span></span>

## <span data-ttu-id="8fe39-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8fe39-110">EXAMPLES</span></span>

### <span data-ttu-id="8fe39-111">Przykład 1. Uruchom zadanie przejęcia awaryjnego dla nazwanego urządzenia i nazwanego urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="8fe39-111">Example 1: Start a failover job for a named device and named target device</span></span>
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Start-AzureStorSimpleDeviceFailoverJob -DeviceName "ChewD_App7" -TargetDeviceName "Fuller05" -Force
a3d902be-8ffb-42a4-bbf8-0a1b30db71b2_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

<span data-ttu-id="8fe39-112">To polecenie pobiera kontenery woluminów trybu failover dla urządzenia o nazwie ChewD_App7 przy użyciu polecenia cmdlet **Get-AzureStorSimpleFailoverVolumeContainers** .</span><span class="sxs-lookup"><span data-stu-id="8fe39-112">This command gets the failover volume containers for the device named ChewD_App7 by using the **Get-AzureStorSimpleFailoverVolumeContainers** cmdlet.</span></span>
<span data-ttu-id="8fe39-113">Polecenie przekazuje wyniki do polecenia cmdlet **WHERE-Object** , które powoduje porzucanie tych kontenerów, które mają wartość inną niż $true dla właściwości **IsDCGroupEligibleForDR** .</span><span class="sxs-lookup"><span data-stu-id="8fe39-113">The command passes the results to the **Where-Object** cmdlet, which drops those containers that have a value other than $True for the **IsDCGroupEligibleForDR** property.</span></span>
<span data-ttu-id="8fe39-114">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Where-Object` .</span><span class="sxs-lookup"><span data-stu-id="8fe39-114">For more information, type `Get-Help Where-Object`.</span></span>
<span data-ttu-id="8fe39-115">Bieżące polecenie cmdlet uruchamia zadania trybu failover dla pozostałych kontenerów woluminu pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="8fe39-115">The current cmdlet starts failover jobs for the remaining failover volume containers.</span></span>
<span data-ttu-id="8fe39-116">Polecenie określa nazwę urządzenia i nazwę urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="8fe39-116">The command specifies the device name and target device name.</span></span>
<span data-ttu-id="8fe39-117">Polecenie zwraca identyfikator wystąpienia zadania uruchamiającego polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fe39-117">The command returns the instance ID of the job that the cmdlet starts.</span></span>

### <span data-ttu-id="8fe39-118">Przykład 2: uruchamianie zadania trybu failover dla urządzenia i urządzenia docelowego określonego przez identyfikator</span><span class="sxs-lookup"><span data-stu-id="8fe39-118">Example 2: Start a failover job for a device and target device specified by ID</span></span>
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Select-Object -First 1 | Start-AzureStorSimpleDeviceFailoverJob -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925" -TargetDeviceId "0ee59ae9-0293-46e2-ae56-bc308c8e5520" -Force
4c5ac0d0-4b66-465c-98f5-aec90505ad12_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

<span data-ttu-id="8fe39-119">To polecenie uzyskuje kontenery woluminów trybu failover dla urządzenia o nazwie ChewD_App7 przy użyciu polecenia **Get-AzureStorSimpleFailoverVolumeContainers**.</span><span class="sxs-lookup"><span data-stu-id="8fe39-119">This command gets the failover volume containers for the device named ChewD_App7 by using **Get-AzureStorSimpleFailoverVolumeContainers**.</span></span>
<span data-ttu-id="8fe39-120">Polecenie przekazuje wyniki do **obiektu WHERE-Object** , który porzuca te osoby, które mają wartość inną niż $true dla właściwości **IsDCGroupEligibleForDR** .</span><span class="sxs-lookup"><span data-stu-id="8fe39-120">The command passes the results to **Where-Object** , which drops those containters that have a value other than $True for the **IsDCGroupEligibleForDR** property.</span></span>
<span data-ttu-id="8fe39-121">Polecenie cmdlet przekazuje wyniki do polecenia cmdlet **Select-Object** , które wybiera pierwszy obiekt, który ma zostać przekazany do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fe39-121">The cmdlet passes the results to the **Select-Object** cmdlet, which selects the first object to pass to the current cmdlet.</span></span>
<span data-ttu-id="8fe39-122">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Select-Object` .</span><span class="sxs-lookup"><span data-stu-id="8fe39-122">For more information, type `Get-Help Select-Object`.</span></span>
<span data-ttu-id="8fe39-123">Bieżące polecenie cmdlet rozpoczyna zadania trybu failover dla wybranego kontenera woluminu trybu failover.</span><span class="sxs-lookup"><span data-stu-id="8fe39-123">The current cmdlet starts failover jobs for the selected failover volume container.</span></span>
<span data-ttu-id="8fe39-124">Polecenie określa identyfikator urządzenia i identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="8fe39-124">The command specifies the device ID and target device ID.</span></span>
<span data-ttu-id="8fe39-125">Polecenie zwraca identyfikator wystąpienia zadania uruchamiającego polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fe39-125">The command returns the instance ID of the job that the cmdlet starts.</span></span>

## <span data-ttu-id="8fe39-126">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8fe39-126">PARAMETERS</span></span>

### <span data-ttu-id="8fe39-127">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="8fe39-127">-DeviceId</span></span>
<span data-ttu-id="8fe39-128">Określa identyfikator wystąpienia urządzenia StorSimple, na którym znajdują się grupy kontenerów woluminów.</span><span class="sxs-lookup"><span data-stu-id="8fe39-128">Specifies the instance ID of the StorSimple device on which the volume container groups exist.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fe39-129">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8fe39-129">-DeviceName</span></span>
<span data-ttu-id="8fe39-130">Określa nazwę urządzenia StorSimple, na którym znajdują się grupy kontenerów woluminów.</span><span class="sxs-lookup"><span data-stu-id="8fe39-130">Specifies the name of the StorSimple device on which the volume container groups exist.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fe39-131">-Force</span><span class="sxs-lookup"><span data-stu-id="8fe39-131">-Force</span></span>
<span data-ttu-id="8fe39-132">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8fe39-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8fe39-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="8fe39-133">-Profile</span></span>
<span data-ttu-id="8fe39-134">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8fe39-134">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="8fe39-135">-TargetDeviceId</span><span class="sxs-lookup"><span data-stu-id="8fe39-135">-TargetDeviceId</span></span>
<span data-ttu-id="8fe39-136">Określa identyfikator wystąpienia urządzenia StorSimple, do którego odbędzie się błąd tego polecenia w grupach kontenerów woluminów.</span><span class="sxs-lookup"><span data-stu-id="8fe39-136">Specifies the instance ID of the StorSimple device to which this cmdlet fails over the volume container groups.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fe39-137">-TargetDeviceName</span><span class="sxs-lookup"><span data-stu-id="8fe39-137">-TargetDeviceName</span></span>
<span data-ttu-id="8fe39-138">Określa nazwę urządzenia StorSimple, na którym jest zawodzi to polecenie cmdlet w grupach kontenerów woluminów.</span><span class="sxs-lookup"><span data-stu-id="8fe39-138">Specifies the name of the StorSimple device to which this cmdlet fails over the volume container groups.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fe39-139">-VolumecontainerGroups</span><span class="sxs-lookup"><span data-stu-id="8fe39-139">-VolumecontainerGroups</span></span>
<span data-ttu-id="8fe39-140">Określa listę grup kontenerów woluminów, które ten polecenie cmdlet może przełączyć na inne urządzenie.</span><span class="sxs-lookup"><span data-stu-id="8fe39-140">Specifies the list of volume container groups that this cmdlet fails over to another device.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe39-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fe39-141">CommonParameters</span></span>
<span data-ttu-id="8fe39-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fe39-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fe39-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fe39-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fe39-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8fe39-144">INPUTS</span></span>

### <span data-ttu-id="8fe39-145">Lista\<DataContainerGroup\></span><span class="sxs-lookup"><span data-stu-id="8fe39-145">List\<DataContainerGroup\></span></span>
<span data-ttu-id="8fe39-146">Do tego polecenia cmdlet można przetworzyć listę grup kontenerów woluminów.</span><span class="sxs-lookup"><span data-stu-id="8fe39-146">You can pipe a list of volume container groups to this cmdlet.</span></span>

## <span data-ttu-id="8fe39-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8fe39-147">OUTPUTS</span></span>

### <span data-ttu-id="8fe39-148">Ciąg</span><span class="sxs-lookup"><span data-stu-id="8fe39-148">String</span></span>

## <span data-ttu-id="8fe39-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8fe39-149">NOTES</span></span>

## <span data-ttu-id="8fe39-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8fe39-150">RELATED LINKS</span></span>

[<span data-ttu-id="8fe39-151">Get-AzureStorSimpleFailoverVolumeContainers</span><span class="sxs-lookup"><span data-stu-id="8fe39-151">Get-AzureStorSimpleFailoverVolumeContainers</span></span>](./Get-AzureStorSimpleFailoverVolumeContainers.md)


