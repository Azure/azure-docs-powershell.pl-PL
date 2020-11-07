---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35b937b810da65cc3cc2ed330198011ec108f9d6
ms.sourcegitcommit: 10ec909100a70acec94d42f6084e7bf0342c6854
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/19/2020
ms.locfileid: "93896853"
---
# <span data-ttu-id="cf5bf-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="cf5bf-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="cf5bf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cf5bf-102">SYNOPSIS</span></span>
<span data-ttu-id="cf5bf-103">Przywracanie kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="cf5bf-103">Restore a backup.</span></span>

## <span data-ttu-id="cf5bf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cf5bf-104">SYNTAX</span></span>

### <span data-ttu-id="cf5bf-105">Backups_Restore (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="cf5bf-105">Backups_Restore (Default)</span></span>
```
Restore-AzsBackup [-ResourceGroupName <String>] -Name <String> [-Location <String>]
 -DecryptionCertPath <String> -DecryptionCertPassword <SecureString> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf5bf-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="cf5bf-106">ResourceId</span></span>
```
Restore-AzsBackup -DecryptionCertPath <String> -DecryptionCertPassword <SecureString> -ResourceId <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf5bf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cf5bf-107">DESCRIPTION</span></span>
<span data-ttu-id="cf5bf-108">Przywracanie kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="cf5bf-108">Restore a backup.</span></span>

## <span data-ttu-id="cf5bf-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cf5bf-109">EXAMPLES</span></span>

### <span data-ttu-id="cf5bf-110">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="cf5bf-110">EXAMPLE 1</span></span>
```
Restore-AzsBackup -Name 4e90bd2f-c7ab-47a3-a3c7-908cddd1ad0e -DecryptionCertPath $decryptionCertPath -DecryptionCertPassword $decryptionCertPassword
```

<span data-ttu-id="cf5bf-111">Przywracanie z kopii zapasowej stosu Azure.</span><span class="sxs-lookup"><span data-stu-id="cf5bf-111">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="cf5bf-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cf5bf-112">PARAMETERS</span></span>

### <span data-ttu-id="cf5bf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf5bf-113">-AsJob</span></span>
<span data-ttu-id="cf5bf-114">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="cf5bf-114">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf5bf-115">-DecryptionCertPassword</span><span class="sxs-lookup"><span data-stu-id="cf5bf-115">-DecryptionCertPassword</span></span>
<span data-ttu-id="cf5bf-116">Hasło certyfikatu deszyfrowania.</span><span class="sxs-lookup"><span data-stu-id="cf5bf-116">Password of the decryption cert.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf5bf-117">-DecryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="cf5bf-117">-DecryptionCertPath</span></span>
<span data-ttu-id="cf5bf-118">Ścieżka do pliku certyfikatu deszyfrującego z kluczem prywatnym (pfx).</span><span class="sxs-lookup"><span data-stu-id="cf5bf-118">Path to the decryption cert file with private key (.pfx).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf5bf-119">-Force</span><span class="sxs-lookup"><span data-stu-id="cf5bf-119">-Force</span></span>
<span data-ttu-id="cf5bf-120">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cf5bf-120">Don't ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf5bf-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cf5bf-121">-Location</span></span>
<span data-ttu-id="cf5bf-122">Nazwa lokalizacji kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="cf5bf-122">Name of location to backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf5bf-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cf5bf-123">-Name</span></span>
<span data-ttu-id="cf5bf-124">Nazwa kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="cf5bf-124">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf5bf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf5bf-125">-ResourceGroupName</span></span>
<span data-ttu-id="cf5bf-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cf5bf-126">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf5bf-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf5bf-127">-ResourceId</span></span>
<span data-ttu-id="cf5bf-128">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="cf5bf-128">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf5bf-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cf5bf-129">-Confirm</span></span>
<span data-ttu-id="cf5bf-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf5bf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf5bf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf5bf-131">-WhatIf</span></span>
<span data-ttu-id="cf5bf-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf5bf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf5bf-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cf5bf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf5bf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf5bf-134">CommonParameters</span></span>
<span data-ttu-id="cf5bf-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf5bf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf5bf-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf5bf-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf5bf-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf5bf-137">INPUTS</span></span>

## <span data-ttu-id="cf5bf-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cf5bf-138">OUTPUTS</span></span>

## <span data-ttu-id="cf5bf-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cf5bf-139">NOTES</span></span>

## <span data-ttu-id="cf5bf-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf5bf-140">RELATED LINKS</span></span>
