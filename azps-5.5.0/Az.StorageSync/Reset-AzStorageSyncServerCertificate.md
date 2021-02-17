---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/reset-Azstoragesyncservercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
ms.openlocfilehash: 41caebb8b43c7c050aef2dac77daf51eebdaf42a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241763"
---
# <span data-ttu-id="c5c3b-101">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="c5c3b-101">Reset-AzStorageSyncServerCertificate</span></span>

## <span data-ttu-id="c5c3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5c3b-102">SYNOPSIS</span></span>
<span data-ttu-id="c5c3b-103">Używaj tylko do rozwiązywania problemów.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-103">Use for troubleshooting only.</span></span> <span data-ttu-id="c5c3b-104">To polecenie spowoduje roll the storage sync server certificate used to describe the server identity to the storage sync service.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-104">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

## <span data-ttu-id="c5c3b-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c5c3b-105">SYNTAX</span></span>

### <span data-ttu-id="c5c3b-106">StringParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="c5c3b-106">StringParameterSet (Default)</span></span>
```
Reset-AzStorageSyncServerCertificate [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5c3b-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5c3b-107">ObjectParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentObject] <PSStorageSyncService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5c3b-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5c3b-108">ParentStringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5c3b-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="c5c3b-109">DESCRIPTION</span></span>
<span data-ttu-id="c5c3b-110">To polecenie spowoduje roll storage sync server certificate used to describe the server identity to the storage sync service.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-110">This command will roll storage sync server certificate used to describe the server identity to the storage sync service.</span></span> <span data-ttu-id="c5c3b-111">Jest to przeznaczone do użycia w scenariuszach rozwiązywania problemów.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-111">This is meant for to be used in troubleshooting scenarios.</span></span> <span data-ttu-id="c5c3b-112">Podczas wywoływania tego polecenia certyfikat serwera jest zamieniany, co pozwala zaktualizować usługę synchronizacji magazynu, w przypadku których jest zarejestrowany ten serwer, przesyłając publiczną część klucza.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-112">When calling this command, the server certificate is replaced, updating the storage sync service this server is registered with as well, by submitting the public part of the key.</span></span> <span data-ttu-id="c5c3b-113">Ponieważ jest generowany nowy certyfikat, aktualizowany jest również czas wygaśnięcia tego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-113">Since a new certificate is generated, the expiration time of this cert is also updated.</span></span> <span data-ttu-id="c5c3b-114">Tego polecenia można także użyć do zaktualizowania wygasłego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-114">This command can also be used to update an expired certificate.</span></span> <span data-ttu-id="c5c3b-115">Może się tak zdarzyć, jeśli serwer jest w trybie offline przez dłuższy czas.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-115">This can happen if a server is offline for an extended period of time.</span></span>

## <span data-ttu-id="c5c3b-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c5c3b-116">EXAMPLES</span></span>

### <span data-ttu-id="c5c3b-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c5c3b-117">Example 1</span></span>
```powershell
PS C:\> Reset-AzStorageSyncServerCertificate -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="c5c3b-118">To polecenie w bezpieczny sposób spowoduje roll certyfikat serwera lokalnego i poinformuje odpowiednią usługę synchronizacji magazynu o nowej tożsamości serwera.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-118">This command will roll the local server certificate and inform the corresponding storage sync service of the server's new identity, in a secure way.</span></span>

## <span data-ttu-id="c5c3b-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5c3b-119">PARAMETERS</span></span>

### <span data-ttu-id="c5c3b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5c3b-120">-DefaultProfile</span></span>
<span data-ttu-id="c5c3b-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5c3b-122">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="c5c3b-122">-ParentObject</span></span>
<span data-ttu-id="c5c3b-123">Obiekt StorageSyncService, który zwykle przechodzi przez parametr.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-123">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5c3b-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c5c3b-124">-ParentResourceId</span></span>
<span data-ttu-id="c5c3b-125">Identyfikator zasobu nadrzędnego usługi StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="c5c3b-125">StorageSyncService Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5c3b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5c3b-126">-PassThru</span></span>
<span data-ttu-id="c5c3b-127">W normalnym wykonaniu to polecenie cmdlet nie zwraca żadnej wartości przy sukcesie.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-127">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="c5c3b-128">Jeśli podasz parametr PassThru, po pomyślnym wykonaniu polecenie cmdlet zapisze wartość w potoku.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-128">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5c3b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5c3b-129">-ResourceGroupName</span></span>
<span data-ttu-id="c5c3b-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5c3b-131">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="c5c3b-131">-StorageSyncServiceName</span></span>
<span data-ttu-id="c5c3b-132">Nazwa usługi StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-132">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5c3b-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c5c3b-133">-Confirm</span></span>
<span data-ttu-id="c5c3b-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5c3b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5c3b-135">-WhatIf</span></span>
<span data-ttu-id="c5c3b-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c5c3b-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5c3b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5c3b-138">CommonParameters</span></span>
<span data-ttu-id="c5c3b-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5c3b-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5c3b-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5c3b-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5c3b-141">INPUTS</span></span>

### <span data-ttu-id="c5c3b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="c5c3b-142">System.String</span></span>

### <span data-ttu-id="c5c3b-143">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="c5c3b-143">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="c5c3b-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5c3b-144">OUTPUTS</span></span>

### <span data-ttu-id="c5c3b-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="c5c3b-145">System.Object</span></span>
## <span data-ttu-id="c5c3b-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c5c3b-146">NOTES</span></span>

## <span data-ttu-id="c5c3b-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c5c3b-147">RELATED LINKS</span></span>
