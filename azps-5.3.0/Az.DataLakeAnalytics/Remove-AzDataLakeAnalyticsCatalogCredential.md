---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 9fbc00fe190e0a53fc9c41a6894ec35a7f8d9129
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489213"
---
# <span data-ttu-id="0de9e-101">Remove-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="0de9e-101">Remove-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="0de9e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0de9e-102">SYNOPSIS</span></span>
<span data-ttu-id="0de9e-103">Usuwa poświadczenia usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0de9e-103">Deletes an Azure Data Lake Analytics credential.</span></span>

## <span data-ttu-id="0de9e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0de9e-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0de9e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0de9e-105">DESCRIPTION</span></span>
<span data-ttu-id="0de9e-106">Polecenie cmdlet Remove-AzDataLakeAnalyticsCatalogCredential usuwa poświadczenia wykazu usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0de9e-106">The Remove-AzDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="0de9e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0de9e-107">EXAMPLES</span></span>

### <span data-ttu-id="0de9e-108">Przykład 1: usuwanie poświadczenia</span><span class="sxs-lookup"><span data-stu-id="0de9e-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="0de9e-109">To polecenie usuwa określone poświadczenia wykazu usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0de9e-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="0de9e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0de9e-110">PARAMETERS</span></span>

### <span data-ttu-id="0de9e-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="0de9e-111">-Account</span></span>
<span data-ttu-id="0de9e-112">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0de9e-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="0de9e-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0de9e-113">-DatabaseName</span></span>
<span data-ttu-id="0de9e-114">Określa nazwę bazy danych, która przechowuje poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="0de9e-114">Specifies the name of the database that holds the credential.</span></span>

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

### <span data-ttu-id="0de9e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0de9e-115">-DefaultProfile</span></span>
<span data-ttu-id="0de9e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0de9e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0de9e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0de9e-117">-Force</span></span>
<span data-ttu-id="0de9e-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0de9e-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0de9e-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0de9e-119">-Name</span></span>
<span data-ttu-id="0de9e-120">Określa nazwę poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="0de9e-120">Specifies the name of the credential.</span></span>

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

### <span data-ttu-id="0de9e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0de9e-121">-PassThru</span></span>
<span data-ttu-id="0de9e-122">Wskazuje, że to polecenie cmdlet nie czeka na zakończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="0de9e-122">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="0de9e-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="0de9e-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0de9e-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="0de9e-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0de9e-125">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="0de9e-125">-Password</span></span>
<span data-ttu-id="0de9e-126">Hasło poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="0de9e-126">The password for the credential.</span></span>
<span data-ttu-id="0de9e-127">Jest to wymagane, Jeśli rozmówca nie jest właścicielem konta.</span><span class="sxs-lookup"><span data-stu-id="0de9e-127">This is required if the caller is not the owner of the account.</span></span>

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

### <span data-ttu-id="0de9e-128">-Rekursywowanie</span><span class="sxs-lookup"><span data-stu-id="0de9e-128">-Recurse</span></span>
<span data-ttu-id="0de9e-129">Wskazuje, że operacja usuwania powinna przekroczyć, a także usunąć i upuścić wszystkie zasoby zależne od tego poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="0de9e-129">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

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

### <span data-ttu-id="0de9e-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0de9e-130">-Confirm</span></span>
<span data-ttu-id="0de9e-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0de9e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0de9e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0de9e-132">-WhatIf</span></span>
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

### <span data-ttu-id="0de9e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0de9e-133">CommonParameters</span></span>
<span data-ttu-id="0de9e-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0de9e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0de9e-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0de9e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0de9e-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0de9e-136">INPUTS</span></span>

### <span data-ttu-id="0de9e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0de9e-137">System.String</span></span>

### <span data-ttu-id="0de9e-138">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="0de9e-138">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="0de9e-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0de9e-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0de9e-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0de9e-140">OUTPUTS</span></span>

### <span data-ttu-id="0de9e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0de9e-141">System.Boolean</span></span>

## <span data-ttu-id="0de9e-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0de9e-142">NOTES</span></span>

## <span data-ttu-id="0de9e-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0de9e-143">RELATED LINKS</span></span>
