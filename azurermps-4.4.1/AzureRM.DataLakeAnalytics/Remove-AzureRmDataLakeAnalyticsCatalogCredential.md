---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: fc25b0a6605632da44d2b198c4bb30c515b2e456
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527626"
---
# <span data-ttu-id="1f83a-101">Remove-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="1f83a-101">Remove-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="1f83a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1f83a-102">SYNOPSIS</span></span>
<span data-ttu-id="1f83a-103">Usuwa poświadczenia usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1f83a-103">Deletes an Azure Data Lake Analytics credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f83a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1f83a-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f83a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1f83a-105">DESCRIPTION</span></span>
<span data-ttu-id="1f83a-106">Polecenie cmdlet Remove-AzureRmDataLakeAnalyticsCatalogCredential usuwa poświadczenia wykazu usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1f83a-106">The Remove-AzureRmDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="1f83a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1f83a-107">EXAMPLES</span></span>

### <span data-ttu-id="1f83a-108">Przykład 1: usuwanie poświadczenia</span><span class="sxs-lookup"><span data-stu-id="1f83a-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="1f83a-109">To polecenie usuwa określone poświadczenia wykazu usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1f83a-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="1f83a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1f83a-110">PARAMETERS</span></span>

### <span data-ttu-id="1f83a-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="1f83a-111">-Account</span></span>
<span data-ttu-id="1f83a-112">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1f83a-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f83a-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1f83a-113">-DatabaseName</span></span>
<span data-ttu-id="1f83a-114">Określa nazwę bazy danych, która przechowuje poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="1f83a-114">Specifies the name of the database that holds the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f83a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1f83a-115">-Force</span></span>
<span data-ttu-id="1f83a-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1f83a-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1f83a-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1f83a-117">-Name</span></span>
<span data-ttu-id="1f83a-118">Określa nazwę poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="1f83a-118">Specifies the name of the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f83a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f83a-119">-PassThru</span></span>
<span data-ttu-id="1f83a-120">Wskazuje, że to polecenie cmdlet nie czeka na zakończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="1f83a-120">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="1f83a-121">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="1f83a-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1f83a-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="1f83a-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1f83a-123">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="1f83a-123">-Password</span></span>
<span data-ttu-id="1f83a-124">Hasło poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="1f83a-124">The password for the credential.</span></span>
<span data-ttu-id="1f83a-125">Jest to wymagane, Jeśli rozmówca nie jest właścicielem konta.</span><span class="sxs-lookup"><span data-stu-id="1f83a-125">This is required if the caller is not the owner of the account.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f83a-126">-Rekursywowanie</span><span class="sxs-lookup"><span data-stu-id="1f83a-126">-Recurse</span></span>
<span data-ttu-id="1f83a-127">Wskazuje, że operacja usuwania powinna przekroczyć, a także usunąć i upuścić wszystkie zasoby zależne od tego poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="1f83a-127">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f83a-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1f83a-128">-Confirm</span></span>
<span data-ttu-id="1f83a-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f83a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f83a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f83a-130">-WhatIf</span></span>
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

### <span data-ttu-id="1f83a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f83a-131">-DefaultProfile</span></span>
<span data-ttu-id="1f83a-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1f83a-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f83a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f83a-133">CommonParameters</span></span>
<span data-ttu-id="1f83a-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f83a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f83a-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f83a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f83a-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f83a-136">INPUTS</span></span>

## <span data-ttu-id="1f83a-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1f83a-137">OUTPUTS</span></span>

### <span data-ttu-id="1f83a-138">logiczną</span><span class="sxs-lookup"><span data-stu-id="1f83a-138">bool</span></span>
<span data-ttu-id="1f83a-139">Jeśli PassThru jest określony, zwraca wartość Prawda po wykonaniu operacji.</span><span class="sxs-lookup"><span data-stu-id="1f83a-139">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="1f83a-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1f83a-140">NOTES</span></span>

## <span data-ttu-id="1f83a-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f83a-141">RELATED LINKS</span></span>

