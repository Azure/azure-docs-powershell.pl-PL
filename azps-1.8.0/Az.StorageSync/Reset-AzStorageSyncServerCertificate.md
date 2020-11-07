---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/reset-Azstoragesyncservercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
ms.openlocfilehash: 4c27cc1cadb7d667793aa297303e539bd8db186f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707438"
---
# <span data-ttu-id="a06b5-101">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="a06b5-101">Reset-AzStorageSyncServerCertificate</span></span>

## <span data-ttu-id="a06b5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a06b5-102">SYNOPSIS</span></span>
<span data-ttu-id="a06b5-103">Służy tylko do rozwiązywania problemów.</span><span class="sxs-lookup"><span data-stu-id="a06b5-103">Use for troubleshooting only.</span></span> <span data-ttu-id="a06b5-104">To polecenie spowoduje wywrócenie certyfikatu serwera synchronizacji magazynu użytego do opisania tożsamości serwera w usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="a06b5-104">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

## <span data-ttu-id="a06b5-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a06b5-105">SYNTAX</span></span>

### <span data-ttu-id="a06b5-106">ObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a06b5-106">ObjectParameterSet (Default)</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentObject] <PSStorageSyncService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a06b5-107">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="a06b5-107">StringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a06b5-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="a06b5-108">ParentStringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a06b5-109">Opis</span><span class="sxs-lookup"><span data-stu-id="a06b5-109">DESCRIPTION</span></span>
<span data-ttu-id="a06b5-110">To polecenie spowoduje przewinięcie certyfikatu serwera synchronizacji magazynu użytego do opisania tożsamości serwera w usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="a06b5-110">This command will roll storage sync server certificate used to describe the server identity to the storage sync service.</span></span> <span data-ttu-id="a06b5-111">Ta funkcja jest przeznaczona do użytku w scenariuszach rozwiązywania problemów.</span><span class="sxs-lookup"><span data-stu-id="a06b5-111">This is meant for to be used in troubleshooting scenarios.</span></span> <span data-ttu-id="a06b5-112">Podczas rozmowy z tym poleceniem certyfikat serwera jest zastępowany, aktualizowanie usługi synchronizacji magazynu, z którą jest on zarejestrowany, oraz przesłanie publicznej części klucza.</span><span class="sxs-lookup"><span data-stu-id="a06b5-112">When calling this command, the server certificate is replaced, updating the storage sync service this server is registered with as well, by submitting the public part of the key.</span></span> <span data-ttu-id="a06b5-113">Po wygenerowaniu nowego certyfikatu czas wygaśnięcia tego certyfikatu również zostanie zaktualizowany.</span><span class="sxs-lookup"><span data-stu-id="a06b5-113">Since a new certificate is generated, the expiration time of this cert is also updated.</span></span> <span data-ttu-id="a06b5-114">Za pomocą tego polecenia można również zaktualizować wygasły certyfikat.</span><span class="sxs-lookup"><span data-stu-id="a06b5-114">This command can also be used to update an expired certificate.</span></span> <span data-ttu-id="a06b5-115">Może się tak zdarzyć, jeśli serwer jest w trybie offline przez dłuższy czas.</span><span class="sxs-lookup"><span data-stu-id="a06b5-115">This can happen if a server is offline for an extended period of time.</span></span>

## <span data-ttu-id="a06b5-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a06b5-116">EXAMPLES</span></span>

### <span data-ttu-id="a06b5-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a06b5-117">Example 1</span></span>
```powershell
PS C:\> Reset-AzStorageSyncServerCertificate -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="a06b5-118">To polecenie porzuci lokalny certyfikat serwera i poinformuje odpowiednią usługę synchronizacji magazynu o nowej tożsamości serwera w bezpieczny sposób.</span><span class="sxs-lookup"><span data-stu-id="a06b5-118">This command will roll the local server certificate and inform the corresponding storage sync service of the server's new identity, in a secure way.</span></span>

## <span data-ttu-id="a06b5-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a06b5-119">PARAMETERS</span></span>

### <span data-ttu-id="a06b5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a06b5-120">-DefaultProfile</span></span>
<span data-ttu-id="a06b5-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a06b5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a06b5-122">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="a06b5-122">-ParentObject</span></span>
<span data-ttu-id="a06b5-123">Obiekt StorageSyncService, zwykle przepuszczany przez parametr.</span><span class="sxs-lookup"><span data-stu-id="a06b5-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="a06b5-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a06b5-124">-ParentResourceId</span></span>
<span data-ttu-id="a06b5-125">Identyfikator zasobu nadrzędnego StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="a06b5-125">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="a06b5-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a06b5-126">-PassThru</span></span>
<span data-ttu-id="a06b5-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a06b5-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a06b5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a06b5-128">-ResourceGroupName</span></span>
<span data-ttu-id="a06b5-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a06b5-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="a06b5-130">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="a06b5-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="a06b5-131">Nazwa StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="a06b5-131">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="a06b5-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a06b5-132">-Confirm</span></span>
<span data-ttu-id="a06b5-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a06b5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a06b5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a06b5-134">-WhatIf</span></span>
<span data-ttu-id="a06b5-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a06b5-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a06b5-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a06b5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a06b5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a06b5-137">CommonParameters</span></span>
<span data-ttu-id="a06b5-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a06b5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a06b5-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a06b5-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a06b5-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a06b5-140">INPUTS</span></span>

### <span data-ttu-id="a06b5-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a06b5-141">System.String</span></span>

### <span data-ttu-id="a06b5-142">Microsoft. Azure. Commands. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="a06b5-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="a06b5-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a06b5-143">OUTPUTS</span></span>

### <span data-ttu-id="a06b5-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="a06b5-144">System.Object</span></span>
## <span data-ttu-id="a06b5-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a06b5-145">NOTES</span></span>

## <span data-ttu-id="a06b5-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a06b5-146">RELATED LINKS</span></span>
